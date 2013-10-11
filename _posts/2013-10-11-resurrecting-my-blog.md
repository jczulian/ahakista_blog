---
layout: post
title:  "Resurrecting my blog"
date:   2013-10-11
categories: 
---


### My first blog

Some time ago, I think it was in 2011, I created my first blog. It was running on a VPS hosted by [kimsufi](http://www.kimsufi.com). This is a low-end VPS service provided by [ovh](http://www.ovh.com/). It was running on Wordpress with a custom theme that I bought on [themeforest](http://www.themeforest.com/).

Everything was just fine and I was publishing blogs regularly. But for some reason earlier this year (2013) I slowly stoped to blog. I guess I was busy with other things. I knew this was just temporary and that I will come back to blogging.

### How I lost my blog

Some weeks ago I wanted to check something on my blog. One of my old post was holding information that I needed. So I went retrieving the blog post only to discover that my blog was not responding. That was not a really big deal, I could find similar information on the internet quite quickly.

As soon as I had some time to dedicate to my blog I wanted to find out how come the blog was offline. It was not too long after that I discovered that the VPS hosting my blog had been destroyed some 2 or 3 months ago.

What happened you might ask? Well the rent for the VPS was on an annual basis. Which means that every year you should pay your rent to be allowed to use the VPS for another year. Surely enough your hoster is sending you an email to remind you that you are reaching slowly the end of you renting period and that if you want to keep on using your VPS you should proceed to a payment in short delays.

The funny thing is that I never received that email. The hoster did is job sending the email though. But that would have been too easy without the _spam filter_. This guy for a reason or another decided that this particular email from my hoster was a spam and surely put it in the spam folder.

Time past by and the dead line arrived without no one noticing anything. The VPS was killed shortly after with all the blog content. Don't worry it was certainly not a big loss for mankind. But still was somehow important to me.

### The autopsy of a dead blog

After a short mourning period I decided to rebuild my blog as I was really motivated to continue bloging and even to do it even more regularly and abundantly than before.

I was not particularly upset against the hoster. Although they could have been more careful: they could have sent more emails or try to call me at least once just to make sure that I was really willing to end my VPS subscription. But for the price you pay, I guess you cannot offer any kind of customer service, beside the strict minimum.

I also asked them if by any chance they wouldn't still have laying around a backup of my system. A database dump would have been enough to restore most of my previous blog posts. But unfortunately they didn't. Everyting went down the kitchen sink for ever.

### Born again

I coudln't actually get a new VPS from kimsufi, because they currently don't have any available for sale.

So I went on a quest for a new cheap hoster. I want it to be cheap because I have really small needs. I just want to basically run a blog. But as I am developer I also want more, I am not satisfied with a simple Wordpress hosting. I want to have root access to a personal machine. I want to be able to install whatever software on it and play with it as much as I want. I also would prefer if the hoster would be located in Europe or in Switzerland. After some researchs I stumble upon [lowendbox](http://lowendbox.com/). This website is great if you are looking for a cheap VPN. Through it I found my new hoster, [Edis](http://www.edis.at/). This hoster is from Austria and have some machines located in Switzerland (in Zűrich). The prices were fair, a bit more expensive than what I paid with kimsufi, but still very affordable.

One problem solved.

Next up: I was not sure if I wanted to continue with Wordpress. Don't get me wrong, I really like Wordpress and I find it to be a really nice piece of software. The thing is that I never really liked writing my blog posts from within Wordpress interface. The interface is great by any account, but it is just that I more a terminal guy than a nice GUI guy, I love text files, I love simple things and simple solutions. I wanted to be able to write my blog posts in Vim, have them saved some where on my laptop disk in a git repository (of course shared on github) and push them easily to the server when ever new content is available.

Enter [Jekyll](http://jekyllrb.com/)! I knew Jekyll for some time but never used it before and as I already had a blog I didn't really have a need for it. But now everything changed, my blog is gone. So I have decided to rebuild the blog on Jekyll. And I really love it so far. It is fast, simple, lighweight and provide enough functionalities for my needs. I am still very new to it so I have no fancy settings or customizations yet, but it will come.

The workflow is really suiting me perfectly. Edit your blog posts in Vim. Save it in git. Push to github. Rsync to VPS. Done. Easy. Fast.

### Hashes...

It is quite funny that one of my previous blog [post]({{ site.url }}/2013/05/03/the-internet-archive.html) was about [The Internet Archive](http://archive.org/). This video is really interesting and I invite you to watch it. One nice thing with The Internet Archive is that they want to be the memory of the internet. So this morning I thought: maybe those guys have a copy of my old website. Although completly improbable they did have 2 snapshots of it. It was not enough to recover all my previous blog posts but I was happy enough to get some back. Basically all posts previous to this one that you can see on the website have been resurrected from my previous blog thanks to The Internet Archive. So a big thanks to The Internet Archive, I was definitely not hoping to find content from my previous website into their archives.

### But didn't you have backups?

Now that's getting a bit embarrassing. As a software developer I should well know that one must do backup of its digital content he cares for. Well I am guilty of not having taken care and time of setting up a proper backup system. I knew that the hoster was doing backups, But I never thought about that the hoster himself would destroy my VPS and its backups. Lesson learn: you should do your own backup, and the more copies you have the better.

With my current system I have four copies of my website:

+ on my laptop
+ on my laptop's backup disk
+ on my github account
+ on the VPS itself, in addition to the generated website

With all that I should have my back covered this time. It is actually not that bad to do mistake. What is really bad is to not learn from your mistake.

### Future plans

As I said earlier my plan is to blog consistently and as much as I can. I like very much writing and I really enjoy going across my blog's archive and read again my posts. They are not of great value for many people, but for me they are like a second memory. I can read about things I have done, videos I have watched and any interesting thing I came across.

I also have plan to install a wiki on this VPS. In it I want to write any kind of content that is not suitable for a blog. I am not yet decided about which software I will use. I have for the moment two contenders: [Dokuwiki](https://www.dokuwiki.org/dokuwiki) and [Gollum](https://github.com/gollum/gollum). Both seem to suit my needs:

+ small
+ simple
+ no database
+ storage into text file
+ no hassle

But that's not for now.
