---
layout: post
title:  "Weekly Review - 2013 Week 43 - 21 October to 27 October"
date:   2013-10-18
categories: 
year: '2013'
month: '10'
start_day: '21'
end_day: '27'
---

This week I have been busy learning Django web framework. I have worked my way through the official [tutorial](https://docs.djangoproject.com/en/1.5/intro/tutorial01/). I have finished it and all the code is on [Github](https://github.com/jczulian/Django_tutorial).

Unfortunately I wasn't able to achieve my blogging goals this week. I have only two blog posts published if we excluded the weekly review one. I will have to organize myself better if I want to be able to publish blog post more frequently.

Also I feel that this week I didn't get enough training. It is somehow missing 1 hour of real physical training. I had plans and time to do it but things turned out differently than what I expected and I couldn't make it to the gym.

### Blog posts 
<ul>
{% for post in site.posts %}
{% capture bday %}{{ post.date | date: '%d' }}{% endcapture %}
{% capture bmonth %}{{ post.date | date: '%m' }}{% endcapture %}
{% capture byear %}{{ post.date | date: '%Y' }}{% endcapture %}
{% if byear == page.year and bmonth == page.month and bday >= page.start_day and bday <= page.end_day %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
{% endif %}
{% endfor %}
</ul>

### Links round-up
- [Reveal.js](https://github.com/hakimel/reveal.js)
    A framework for easily creating beautiful presentations using HTML. Check out the live demo.
- [A Symfony2 tutorial to build a blog engine](http://tutorial.symblog.co.uk/docs/configuration-and-templating.html)
- [A translation to Symfony2 of the famous Jobeet tutorial originaly from Symfony 1](http://www.ens.ro/2012/03/21/jobeet-tutorial-with-symfony2/)
- [The Expression Language component is arriving in Symfone 2.4](http://www.sensiolabs.co.uk/blog/simplifying-the-life-of-developers)


- [A text editor in node-webkit](https://github.com/zcbenz/brackets)
- [A presentation about node-webkit](https://speakerdeck.com/zcbenz/node-webkit-app-runtime-based-on-chromium-and-node-dot-js)
- [How to use sqlite to read data from firefox cookies file](http://stackoverflow.com/questions/7610896/how-to-use-sqlite-to-read-data-from-the-firefox-cookies-file)
- [On github organization](http://www.fastcolabs.com/3020181/open-company/inside-githubs-super-lean-management-strategy-and-how-it-drives-innovation)
- [Tulip: Python Asyn I/O library presentation by Guido](https://www.dropbox.com/s/essjj4qmmtrhys4/SFMeetup2013.pdf)
- [Kivy - Open source Python library for rapid development of applications that make use of innovative user interfaces, such as multi-touch apps.](http://kivy.org/#home)
- [Tango With Django - A beginner's guide to web development with Django 1.5.4.](http://www.tangowithdjango.com/)
- [Please stop pretending PHP is a good language](http://edorian.github.io/2013-10-19-Please-stop-pretending-PHP-is-a-good-language/)

### Sport
- 15 minutes running
- 1 hour kickboxing
- 1 hour yoga

### Watching
- [Wolf Children](http://en.wikipedia.org/wiki/Wolf_Children)
- [SymfonyLive London 2013 - Rowan Merewood - Building Better Developper](http://www.youtube.com/watch?v=WTLqfIjJFEI)
- [Mihaly Csikszentmihalyi: Flow, the secret to happiness](http://www.ted.com/talks/mihaly_csikszentmihalyi_on_flow.html)
- [How to train your dragon](http://en.wikipedia.org/wiki/How_to_Train_Your_Dragon_(film\))

### Listening
- Lykke li
- Moderat - II
- Moderat - Moderat
- Calexico - Hot Rails
- Cesaria Evora - Camden Collection
- Stromae - Racine Carée
