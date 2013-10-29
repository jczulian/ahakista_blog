---
layout: post
title:  "Weekly Review - 2013 Week 43 - 21 October to 27 October"
date:   2013-10-27
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

### Tabs sweeping

[Clojure Understood: the Rush Hour Platform](http://michaeldrogalis.tumblr.com/post/65274692089/clojure-understood-the-rush-hour-platform)
[The Essence of ClojureScript](http://swannodette.github.io/2013/10/27/the-essence-of-clojurescript/)
[focus@will](https://www.focusatwill.com/music/#player)
[9 Enhancements to Shell and Vim Productivity | Daniel Miessler](http://www.danielmiessler.com/blog/enhancements-to-shell-and-vim-productivity)
[robbyrussell/oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)
[Drawing Dynamic Visualizations on Vimeo](http://vimeo.com/66085662)
[Ryan Coogler: 6 talks that inspired me | TED Playlists | TED](http://www.ted.com/playlists/132/ryan_coogler_6_talks_that_ins.html?utm_source=newsletter_weekly_2013-10-12&utm_campaign=newsletter_weekly&utm_medium=email&utm_content=playlist_title)
[Glenn Close: The talks that moved me | TED Playlists | TED](http://www.ted.com/playlists/34/glenn_close_the_talks_that_mo.html)
[How We Use Asana - Best Practices for Better Teamwork](http://blog.asana.com/2013/10/best-practices-event/?utm_medium=email&utm_source=Asana&utm_campaign=3234057_October+Newsletter&dm_i=1L9Q,1XBEX,C25THS,6WUDX,1)
[How to Tango with Django: A Python Django Tutorial](http://www.tangowithdjango.com/?utm_source=Python+Weekly+Newsletter&utm_campaign=61dcf803fc-Python_Weekly_Issue_110_October_24_2013&utm_medium=email&utm_term=0_9e26887fc5-61dcf803fc-312686705)
[OpenTechSchool – Introduction to Data Processing with Python](http://opentechschool.github.io/python-data-intro/?utm_source=Python+Weekly+Newsletter&utm_campaign=61dcf803fc-Python_Weekly_Issue_110_October_24_2013&utm_medium=email&utm_term=0_9e26887fc5-61dcf803fc-312686705)
[Learn Python the Hard Way: A Very Simple Introduction to the Terrifyingly Beautiful World of Computers and Code, 3rd Edition | InformIT](http://www.informit.com/store/learn-python-the-hard-way-a-very-simple-introduction-9780321884916?WT.mc_id=IT_NL_Promotions_2013_10_24)
[The Pragmatic Bookshelf | The Coding Dojo Handbook](http://pragprog.com/book/ebdojo/the-coding-dojo-handbook)
[What's new in PhpStorm 7?](http://www.jetbrains.com/phpstorm/whatsnew/index.html?utm_source=phpstorm7&utm_medium=newsletter&utm_campaign=phpstorm&utm_content=ce)
[Using the PhpStorm built-in SSH terminal and remote SSH external tools | JetBrains PhpStorm Blog](http://blog.jetbrains.com/phpstorm/2013/08/using-the-phpstorm-built-in-ssh-terminal-and-remote-ssh-external-tools/)
[Private group chat and IM, business and team collaboration - HipChat](https://www.hipchat.com/)
[Write a NES Emulator with JavaScript - Part 1 - Alexander Dickson](http://blog.alexanderdickson.com/javascript-nes-emulator-part-1?utm_source=javascriptweekly&utm_medium=email)
[linuxerwang/goats-html](https://github.com/linuxerwang/goats-html)
[Built In Interfaces](http://jmoiron.net/blog/built-in-interfaces/)
[free-programming-books/free-programming-books.md at master · vhf/free-programming-books](https://github.com/vhf/free-programming-books/blob/master/free-programming-books.md#professional-development)
[Interactive Data Visualization for the Web](http://chimera.labs.oreilly.com/books/1230000000345/index.html)
[RoboVM - Develop iPhone and iPad Apps in Java with RoboVM](http://www.robovm.org/)
[Announcements | Programming Languages](https://class.coursera.org/proglang-002/class/index?utm_classid=970860&utm_nottype=class.generic&utm_notid=2907&utm_linknum=1)
[Write your own ORM on top of Doctrine2 — Doctrine-Project](http://www.doctrine-project.org/blog/your-own-orm-doctrine2.html)
[in which we return to the realm of the bactrian - Technomancy](http://technomancy.us/170)
[Parallel Universe • No More Callbacks: 10,000 Actors, 10,000 Threads, 10,000 Spaceships](http://blog.paralleluniverse.co/post/64210769930/spaceships2)
[How Extreme Transparency Can Make Your Team Its Most Productive | Fast Company | Business + Innovation](http://www.fastcompany.com/3006798/work-smart/how-extreme-transparency-can-make-your-team-its-most-productive?utm_source=Software+Lead+Weekly&utm_campaign=f6afd11db9-Issue_47_11_Oct_2013&utm_medium=email&utm_term=0_efe3d3cd5b-f6afd11db9-123684785)
[Ryan Coogler: 6 talks that inspired me | TED Playlists | TED](http://www.ted.com/playlists/132/ryan_coogler_6_talks_that_ins.html)
[Typing Practice - free games to improve your typing speed - 10FastFingers.com](http://10fastfingers.com/practice#top1000)
[Dan Pink: My 5 favorite talks on work | TED Playlists | TED](http://www.ted.com/playlists/133/dan_pink_my_5_favorite_talks.html?utm_source=newsletter_weekly_2013-09-28&utm_campaign=newsletter_weekly&utm_medium=email&utm_content=playlist_title)
[Twitter](https://twitter.com/)
[lockrun - Run cron job with overrun protection](http://www.unixwiz.net/tools/lockrun.html)
[supervisord at DuckDuckGo](https://duckduckgo.com/?q=supervisord&t=canonical)
[How and Why to Be a Leader (Not a Wannabe) - Umair Haque - Harvard Business Review](http://blogs.hbr.org/2013/07/how-and-why-to-be-a-leader-not/?utm_source=Software+Lead+Weekly&utm_campaign=826872a85e-Issue_45_27_Sep_2013&utm_medium=email&utm_term=0_efe3d3cd5b-826872a85e-123684785)
[7 command-line tools for data science](http://jeroenjanssens.com/2013/09/19/seven-command-line-tools-for-data-science.html)
[jq](http://stedolan.github.io/jq/)
[99 percent invisible at DuckDuckGo](https://duckduckgo.com/?q=99+percent+invisible&t=canonical)
[Asana](https://app.asana.com/)
[Django Packages : Django Packages reusable apps, sites and tools directory](https://www.djangopackages.com/)
[mozilla playdoh at DuckDuckGo](https://duckduckgo.com/?q=mozilla+playdoh&t=canonical)
[robbyrussell/oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)
[start [ZshWiki]](http://zshwiki.org/home/)
[A week of symfony #351 (16->22 September 2013) - Symfony](http://symfony.com/blog/a-week-of-symfony-351-16-22-september-2013)
[Drupal 7 vs Symfony 2: overview after 1 year of Symfony development | Drupal and Symfony2 developers and designers you were trying to find: Pixeljets](http://pixeljets.com/blog/drupal-7-vs-symfony-2-overview-after-1-year-symfony-development)
[Symfony2: as good as PHP gets? | GreenAsh](http://greenash.net.au/thoughts/2013/10/symfony2-as-good-as-php-gets/)
[Announcements — IPython](http://ipython.org/)
[PhpStorm 7.0 released: PHP 5.5, Vagrant, SSH console, debugger config validation, Drupal, frameworks & more | JetBrains PhpStorm Blog](http://blog.jetbrains.com/phpstorm/2013/10/phpstorm-7-0-released-php-5-5-vagrant-ssh-console-debugger-config-validation-drupal-frameworks-more/)
[String](http://caml.inria.fr/pub/docs/manual-ocaml/libref/String.html)
[Unix system programming in OCaml](http://ocamlunix.forge.ocamlcore.org/)
[Unix](http://caml.inria.fr/pub/docs/manual-ocaml/libref/Unix.html#TYPEopen_flag)
[OCaml Journal: The Essence of Functional Programming](file:///home/jc/work/project/ocaml/ocaml-journal/www.ffconsultancy.com/products/ocaml_journal/subscribers/essence.html)
[OCaml Journal: Implementing a simple XML-RPC client and server](file:///home/jc/work/project/ocaml/ocaml-journal/www.ffconsultancy.com/products/ocaml_journal/subscribers/xmlrpc.html)
[Objective CAML Tutorial](http://mirror.ocamlcore.org/ocaml-tutorial.org/)
[ocaml janestreet core at DuckDuckGo](https://duckduckgo.com/?q=ocaml+janestreet+core&t=canonical)
[Open Source @ Jane Street](http://janestreet.github.io/)
[OCaml :: 99 Problems (solved) in OCaml](http://ocaml.org/tutorials/99problems.html)
[OCaml :: Tutorials](http://ocaml.org/tutorials/)
[PLEAC-Objective CAML](http://pleac.sourceforge.net/pleac_ocaml/)
[ocaml how to print list at DuckDuckGo](https://duckduckgo.com/?q=ocaml+how+to+print+list&t=canonical)
[how to generate ocaml ragel at DuckDuckGo](https://duckduckgo.com/?q=how+to+generate+ocaml+ragel&t=canonical)
[The Caml Hump: General purpose libraries :: Lexing and parsing](http://caml.inria.fr/cgi-bin/hump.en.cgi?sort=0&browse=96)
[The Caml Hump: Ragel](http://caml.inria.fr/cgi-bin/hump.en.cgi?contrib=771)
[Stream parser with Ragel and Ruby [Brighter Planet's Safety in Numbers]](http://numbers.brighterplanet.com/2011/06/14/stream_parser_with_ragel_and_ruby/)
[A simple intro to writing a lexer with Ragel.](http://thingsaaronmade.com/blog/a-simple-intro-to-writing-a-lexer-with-ragel.html)
PHP Notice:  Undefined property: stdClass::$title in /home/jc/bin/firefox_tabs.php on line 14
[](http://code.whytheluckystiff.net/hpricot/)
[Adjustable type definitions for data exchange](http://mjambon.com/atd-biniou-intro.html)
[Debian -- Package Search Results -- ocaml](http://packages.debian.org/search?keywords=ocaml&searchon=all&suite=testing&section=all)
[utop/README.md at master · diml/utop](https://github.com/diml/utop/blob/master/README.md)
[zed/src/zed_edit.ml at master · diml/zed](https://github.com/diml/zed/blob/master/src/zed_edit.ml)
[Eliom](http://ocsigen.org/eliom/)
[Ocsigen Tutorial](https://ocsigen.org/tutorial/application)
[TyXML](https://ocsigen.org/tyxml/api/Html5.F)
[core/lib/command.ml at master · janestreet/core](https://github.com/janestreet/core/blob/master/lib/command.ml)
[How to install Django | Django documentation | Django](https://docs.djangoproject.com/en/1.5/topics/install/#installing-official-release)
[Welcome to Django](http://127.0.0.1:8000/)
PHP Notice:  Undefined property: stdClass::$title in /home/jc/bin/firefox_tabs.php on line 14
[](http://127.0.0.1:8000/polls/)
[pycharm at DuckDuckGo](https://duckduckgo.com/?q=pycharm&t=canonical)
[GitHub](https://github.com/)
