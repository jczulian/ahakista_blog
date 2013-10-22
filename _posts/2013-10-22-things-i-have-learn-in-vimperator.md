---
layout: post
title:  "New things I have learn with Vimperator"
date:   2013-10-22
categories: 
---

I have been using Vimperator for many years now. But even though I still learn new tricks and shortcuts now and then. And every time I do, it is always a great opportunity to be faster and more efficient at what I do [with a browser of course].

I have been using Vim-like keybindings for more than 5 years. At the beginning it was only from within Vim itself. After getting use to it, it became really painful to operate anything else, like a browser, a terminal, the filesystem, with something that doesn't have vim keybinding. 'j' and 'k' have become synonyms to 'up' and 'down' in my hand's muscle. So much that it is extremely irritating to type 'j' and to see many 'j' letters appearing on the screen instead of having my cursor going down.

Nowadays I don't write much code in Vim. I use instead PhpStorm (which is also another awesome tool). But I have the Vim plugin installed for PhpStorm. Even though PhpStorm is a wonderful tool it would be extremely painful for me to use it without vim keybindings.

I still use vim in many occasions. All my blog posts for example are typed in Vim. Many of my emails also. I ofter use the 'Ctrl+I' shortcut of Vimperator to open up input field found on a web page into vim to edit them.

Even on my terminal (gnome-terminal) I am using vim shortcuts. To activate them you have to set it like so:

{% highlight bash %}
set -o vi
{% endhighlight %}

As I was saying in the beginning I recently discovered some new keybindings for Vimperator. The best way to check time to time if you are still on top of your tools is to have a quick look at the documentation and spend some time reading it [again].

One of the main thing you will want to do with Vimperator is to disable it. I mean it, not joking. Some time some applications provide already great keybindings and Vimperator's keybindings are just interacting badly with the original ones. Such websites include for example your web based email application, like gmail or fastmail.

For some time I have been using a little piece of configuration I found on the web in order to disable automatically Vimperator keybindings every time I would visit those web sites:

{% highlight bash %}
autocmd LocationChange .*                             js modes.passAllKeys = false
autocmd LocationChange www\\.fastmail\\.fm            js modes.passAllKeys = true
autocmd LocationChange mail\\.google\\.com            js modes.passAllKeys = true
{% endhighlight %}

These autocommands are run every time you switch tab or browser window. In you are langing on gmail or fastmail vimperator will turn off its keybindings, in other cases it will activate them.

It turns out there is a better way to achieve this. You could use the 'ignorekeys' command. With it you can add, remove, list and clear the list of web sites that should ignore Vimperator keybindings. Here is the equivalent configuration I have for ignoring Vimperator keybindings in web based email clients.

{% highlight bash %}
:ignorekeys list
gmail
mail.google.com
www.fastmail.fm
{% endhighlight %}

You can add as many sites you'd like. One might want to add to this list also tools like Jira or Confluence as they also provide quite good keybindings.

One other thing I have discovered recently is to copy/paste the current URL you are on. Previously I was doing something really awkward: Ctrl+O to enter url edit mode, then selecting the url with Ctrl + left arrow, and finally Ctrl+c to copy. Really awkward and slow. I knew that there must be another better way to do such a basic thing, but I didn't took the time to look for it. Until one day I got fed up to do this awkward combination for the 20th time during the day. I went straight to the documentation (:help) and in a matter of few minutes found how to perform this task in the right way. Just type 'y'. I can't believe I put off for so long with my less-than-optimal way of copying current URL when such a simple way of doing it existed.

I guess I had come across the 'y' command before when I first learned Vimperator. But then for some reason I must have not used it for some time and I forgot about it. Also I must admit that for a couple of  years I used Chrome with the Vimium plugin which I find much less polished and finished than Vimperator. That might explain why I forgot the 'y'. But now that I have found it again I am putting it to good use every single day.

So the bottom line of all this would be:
- know your tool
- read the documentation
- read the documentation every now and them to keep your tool sharp


