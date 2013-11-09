---
layout: post
title:  "Phpstorm class renaming refactoring"
date:   2013-11-09
categories: 
---

PhpStorm is a well known IDE for the PHP language. It is a spin off product from the Java IDE made by Jetbrain, IntelliJ.

Jetbrain started IntelliJ as a refactoring tool for Java and then moved on to make it a full-blown IDE. Now they produce on this base IDE for Ruby, Python, PHP and other languages.

We should guess that one of the strong point of the IDE is refactoring seeing its inheritance tree. The other day at work I was in need to do some rather simple refactoring. I wanted to rename a class. I was actually surprised to encounter some cases where the refactoring didn't work. 

The class renaming refactoring is in charge of changing the name of your class but also to figure out where this class name is used in your project and to change those references to it too. There are also options to tell the tool that it should also look inside code comments and perform the renaming also in those cases.

From my experience I have found the refactoring tool really good at doing this renaming job. Until now I haven't encounter a case where it actually missed renaming the class and references to it.

But I found one place where it "failed". I put the work in double quote because I believe it is an intentional failure.

In PHP fully qualified class name are separated by backslashes. This would be a valid class name:

{% highlight php %}
use Symfony\Component\HttpFoundation\Response;
{% endhighlight %}

It simply says that you want to use the Response class from the HttpFoundation of Symfony's component. It is very much similar to what you would write in Java, Ruby or Python except that the separator between package names is the backslash.

When you want to talk about a class name in a PHP string you would have to do it like so:
{% highlight php %}
$myClass = "Symfony\\Component\\HttpFoundation\\Response";
{% endhighlight %}

You have to double the backslashes.

But in one of our project we where talking about PHP class naming them without the double backslash:
{% highlight php %}
// how you should normally reference class in a string
$class = "Mysite\\CoreBundle\\Admin\\PageAdmin";

// how we were doing it
$class = 'Mysite\CoreBundle\Admin\PageAdmin';
{% endhighlight %}

The reason why we were doing it like this instead of using the standard double backslash is that the string was intended to be stored into our database, PhpCR. PhpCR is a Content Repository in the JCR way but done in PHP instead of Java. And in PhpCR the way to talk about a class ii to name your class with a single backslash.

So after the refactoring tool run I thought that the code was all good, that all instances of my class name have been replaced with the new name. But it only took few minutes before I started seeing exceptions because some part of the code was trying to use the old class.

Of course I did then a text search on the whole project code base to find out who could still use the old class name. And surely enough I found those two or three strings in which the class name was not given with double backslahes but single one.

I have no idea if this is a voluntary omission from PhpStorm or if they just didn't think that it could be possible to use class names in string with only one single backslash. In any case I will fill a bug report and let them decide if they should add this particular case to their class renaming refactoring tool or not.
