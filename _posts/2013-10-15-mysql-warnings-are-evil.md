---
layout: post
title:  "MySql warnings are evil"
date:   2013-10-15
categories: 
---

Today I was working on our own time-tracking system. This one is build on PHP and stores its data in a MySql database.

The task was to add an entry to a drop down list. This list contains all the billing schemes we use (monthly, quarterly, every six months and so on). So we basically wanted to add another biliing scheme. This seems to be a pretty easy task at first sight.

So I proceed quickly to find out where all those billing schemes were defined and where the form displaying it was produced. Once found I added this new entry to the list. On to the web page the new item appeared on the list as expected.

Then started the problem. For some unknown reasons the form would not be saved properly to the database when selecting the new billing scheme. All the other billing scheme were working fine but not the new one.

I thought for a while that I must have forgotten to define this new scheme to some other places. I started looking for this missing place but couldn't find anything in the code or the configuration. It puzzled me for some time and I have also lost quite some time trying to figure out why this particular billing scheme couldn't be properly saved. It is at the end just a string like the others that I want to save in the database.

I looked in the log files to find some traces of errors but I found absolutely nothing, I tried to debug the application, an stepped into the code responsible for collecting the form data and then to save it into the database. I could actually see the string just before it was sent to the database. Still nothing to be found. And still no string saved into the database.

I just couldn't understand how this could be possible. Then it hit me like a truck on the highway: it must be a enum field in the database. And indeed I could confirm that after asking MySql to describe the table where I was trying to save my data. This column was defined as a [Mysql enum][mysql-enum-doc] which means basically that it only accepts a predefined set of values.

Then to verify this assumption quickly I issue a small SQL statement trying to save into this table some data giving some wrong string to the enum field. And then surprise surprise. MySql didn't really complained. He did but in a rather unusual way.

Here is the output I got on the MySql prompt:

{% highlight sql %}
mysql> update projects set billinginfo = 'blabla' where id = 1676;
Query OK, 0 rows affected, 1 warning (0.00 sec)
Rows matched: 1  Changed: 0  Warnings: 1
{% endhighlight %}

Doesn't look like an error, right? Usually MySql errors look like that:

{% highlight sql %}
mysql> select foo from bar;
ERROR 1146 (42S02): Table 'foodb.bar' doesn't exist
{% endhighlight %}

Here you can clearly see that something went wrong. The first word makes it very obvious, isn't it?

But in the current case you have to read carefully the output. It reads:
{% highlight sql %}
Query OK, 0 rows affected, 1 warning (0.00 sec)
Rows matched: 1  Changed: 0  Warnings: 1
{% endhighlight %}

 What the heck is that warning thing, I never came across it before. Onto the internet to figure out a bit more about these MySql warnings. I found that [page from MySql documentation][mysql-warning-doc] explaining what warnings are and how to actually see them when they occur. Just type in:

{% highlight sql %}
mysql> show warnings;
+---------+------+--------------------------------------------------+
| Level   | Code | Message                                          |
+---------+------+--------------------------------------------------+
| Warning | 1265 | Data truncated for column 'billinginfo' at row 1 |
+---------+------+--------------------------------------------------+
1 row in set (0.00 sec)
{% endhighlight %}

And here come your error message, or should I say your warning message. The message is quiet obscure and doesn't really explain what went wrong. But I already knew what went wrong so it was not to hard here.

So what is happening is rather not nice, at least it doesn't seem really appealing to me.

You try to insert some bogus data into your table, but you don't know yet that the data is bogus. The data is bogus because the table contains an Enum type column for which a set of correct value has been defined. Then Mysql instead of throwing an error and yelling at you just "silently" don't insert the data and issue a warning. 

When you are at the prompt it is quiet hard to see that there is a warning compared to when there is an error. But when you are using this SQL statement from within your application (in my case a PHP application) you just have no feedback at all. No errors, no exception, no messages in php log file, no messages in MySql log file, nada, niet. How bad is that? To my taste extremely bad.

Then to make matter worse: say that you want to update an already existing record and change this particular field with data not defined in the enum. You still won't receive any errors from MySql but it will happily wipe out the previous value that was stored and leave it empty. All that without telling anything to you. Now this is extremely bad, evil, please don't, never do that.

I actually did some research and so far I haven't found a way to handle warnings properly in the application code. Some people recomend running a 'SHOW WARNINGS' statement after each query but I hardly consider that to be solution. I also tried to find out if there is some MySql configuration option that would turn any warning into a real error, but didn't find anything. There is a [question][how-to-deal-with-warning-pdo] related to this topic on StackOverflow but there seems to be no real answer yet to this particular question

To conclude I really think that these warnings are a bad thing. They don't really help you, they corrupt your data and you cannot handle them properly in your application code.


[mysql-warning-doc]: https://dev.mysql.com/doc/refman/5.0/en/show-warnings.html
[how-to-deal-with-warning-pdo]: http://stackoverflow.com/questions/17276811/show-warnings-in-mysql-pdo
[mysql-enum-doc]: https://dev.mysql.com/doc/refman/5.0/en/enum.html
