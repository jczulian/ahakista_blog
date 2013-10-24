---
layout: post
title:  "How to trap emails sent from your development environment"
date:   2013-10-24
categories: 
---

It is often the case that when you are working on some website that you want it to send email to its users. Be it for email confirmation or information of any kind.

The problem is that when you work on a development environment you really don't want those emails to be really sent. Especially if you are working with a copy of the live system database and all users in it are actual real persons. You really don't want your users to receive email about their account deletion because you are working on the deletion process of the website.

Many people would say that you should not work with real data and that you should always use test data while developing. Unfortunately this is some time not possible. Usually for historical reasons the only set of data available is the one currently existing on the live system. One advantage of that is that you have a data set that is completely realistic, both by its size and the coherence of the data it contains. I found in many occasions that working with a copy of the real database is extremely comfortable and useful.

If you have to work with a copy of the original data you can easily change all email address in the database and replace it by yours. Although this will prevent undesirable emails to be sent you won't be able to tell if the email would have be sent to the correct person as now there is only one email address for every one in registered in your database. The other problem that makes this solution often impracticable is that often the email field in the database must be unique so you just cannot have thousands of users having the same email address.

Another slightly different approach would be to generate different email address for every users. Here the problem is slightly different as the emails will be send but never arrive to any inbox. This is really unfortunate especially if you need to check how the message looks in the email or if you want to make sure upon which occasion such and such message are being sent.

Another one is to use a mail system like Swiftmail. This piece of software is being used in Symfony since version 1 of the framework. It has many features and one of them is that you can switch the delivery mechanism. When you are on prod you would activate a real delivery mechanism, like sendmail but when you are on the testing server or on development environment you would use a fake delivery mechanism, resulting in the email not being sent. Everything would behave as if the email would be sent: nothing in your code will take special behavior depending on your environment, there won't be any fake address in the database, there won't be any piece of code replacing every email address by a well defined one. The nice thing is that, at least with Symfony, you can still see the email that should have been sent in the debugger tool bar. So you can actually check that the email was sent at the right time with the correct message.

Yet another solution to this problem is to have a little shell script that will sit between php and your email sending software. This script will be in charge of catching any emails been sent out, change the recipient address to a predefined one and put the originals recipients address into a specific header. This solution is really elegant and simple. For one thing you just have to do this setting only once and then you can forget about it. All emails that you will eventually send from your application, or applications (as you may be working on more than one project) will be trapped and resent to the one email address you would have specified (ideally you own email address).

The setting is rather simple. You first have to change the sendmail variable in your php.ini file to point to the script that will handle the email and then pipe it to sendmail (or your email sending program of choice).

{% highlight bash %}
sendmail_path=/usr/local/bin/trapmail
{% endhighlight %}


Then you create the /usr/local/bin/trapmail with the following line in it.
{% highlight bash %}
formail -R to X-original-to -R cc X-original-cc -R bcc X-original-bcc -f -A "To: devteam@example.com" ¦ /usr/sbin/sendmail -t -i
{% endhighlight %}

The only thing this script does is to change the original header of your emails. It saves the original recipients into another email's header and replace to TO header with your email address.

I have been using this solution for some years now. When I am not working on a Symfony project I have in many occasion found it extremely valuable and helpful.
