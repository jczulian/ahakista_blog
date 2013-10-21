---
layout: post
title:  "Weekly Review - 2013 Week 42 - 14 October to 20 October"
date:   2013-10-18
categories: 
year: '2013'
month: '10'
start_day: '14'
end_day: '20'
---

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
- [A text editor in node-webkit](https://github.com/zcbenz/brackets)
- [A presentation about node-webkit](https://speakerdeck.com/zcbenz/node-webkit-app-runtime-based-on-chromium-and-node-dot-js)
- [How to use sqlite to read data from firefox cookies file](http://stackoverflow.com/questions/7610896/how-to-use-sqlite-to-read-data-from-the-firefox-cookies-file)

### Sport
- one hour kickboxing training
- one hour BodyPump
- running: 3 kilometers in 16 minutes
- capoeira roda

### Music
- Grouve armada - The Best Of
- Oh Land - Whishbone

### Ideas
php script to read firefox's session file and get the list of open tabs


### Small things
[How to set solarized theme on Gnome Terminal](http://www.webupd8.org/2011/04/solarized-must-have-color-paletter-for.html)

### Tabs sweeping

- [StrangeLoop2013/slides/sessions/Odersky-TroubleWithTypes.pptx at master · strangeloop/StrangeLoop2013](https://github.com/strangeloop/StrangeLoop2013/blob/master/slides/sessions/Odersky-TroubleWithTypes.pptx)
- [Write your own ORM on top of Doctrine2 — Doctrine-Project](http://www.doctrine-project.org/blog/your-own-orm-doctrine2.html)
- [in which we return to the realm of the bactrian - Technomancy](http://technomancy.us/170)
- [Parallel Universe • No More Callbacks: 10,000 Actors, 10,000 Threads, 10,000 Spaceships](http://blog.paralleluniverse.co/post/64210769930/spaceships2)
- [WebRTC: Plugin-free Realtime Communication - YouTube](http://www.youtube.com/watch?v=3Ifbqaw5l_I)
- [Monthly review: September 2013 » sacha chua :: living an awesome lifesacha chua :: living an awesome life](http://sachachua.com/blog/2013/10/monthly-review-september-2013/)
- [How Extreme Transparency Can Make Your Team Its Most Productive | Fast Company | Business + Innovation](http://www.fastcompany.com/3006798/work-smart/how-extreme-transparency-can-make-your-team-its-most-productive?utm_source=Software+Lead+Weekly&utm_campaign=f6afd11db9-Issue_47_11_Oct_2013&utm_medium=email&utm_term=0_efe3d3cd5b-f6afd11db9-123684785)
- [Full List | Best iPhone Apps | TIME.com](http://techland.time.com/2013/09/20/50-best-iphone-apps-2013-edition/slide/all/)
- [Ryan Coogler: 6 talks that inspired me | TED Playlists | TED](http://www.ted.com/playlists/132/ryan_coogler_6_talks_that_ins.html)
- [Dan Pink: My 5 favorite talks on work | TED Playlists | TED](http://www.ted.com/playlists/133/dan_pink_my_5_favorite_talks.html?utm_source=newsletter_weekly_2013-09-28&utm_campaign=newsletter_weekly&utm_medium=email&utm_content=playlist_title)
- [A bitter taste](https://kotka.de/blog/2013/10/A_bitter_taste.html)
- [Elephant in the Room](http://elephantintheroom.io/)
- [lockrun - Run cron job with overrun protection](http://www.unixwiz.net/tools/lockrun.html)
- [mojombo/mojombo.github.io](https://github.com/mojombo/mojombo.github.io)
- [Sites · mojombo/jekyll Wiki](https://github.com/mojombo/jekyll/wiki/sites)
- [plug/plugfr.org](https://github.com/plug/plugfr.org/)
- [PLUG – Provence Linux User Group](http://plugfr.org/)
- [How and Why to Be a Leader (Not a Wannabe) - Umair Haque - Harvard Business Review](http://blogs.hbr.org/2013/07/how-and-why-to-be-a-leader-not/?utm_source=Software+Lead+Weekly&utm_campaign=826872a85e-Issue_45_27_Sep_2013&utm_medium=email&utm_term=0_efe3d3cd5b-826872a85e-123684785)
- [New Feature – Save Links and Notes Through Email | Diigo Blog](http://blog.diigo.com/2013/09/27/save-links-and-notes-through-email/)
- [How to Backup Linux? 15 rsync Command Examples](http://www.thegeekstuff.com/2010/09/rsync-command-examples/)
- [Sass - Wikipedia, the free encyclopedia](http://en.wikipedia.org/wiki/Sass)
- [zcbenz/brackets](https://github.com/zcbenz/brackets)
- [gothfox/Tiny-Tiny-RSS](https://github.com/gothfox/Tiny-Tiny-RSS)
- [Roadmap - Symfony](http://symfony.com/roadmap)
- [Toodledo : Tasks, notes, outlines and lists](http://www.toodledo.com/)
- [dokuwiki [DokuWiki]](https://www.dokuwiki.org/dokuwiki)
- [Some Jekyll Hacks - Brizzled](http://brizzled.clapper.org/blog/2010/12/20/some-jekyll-hacks/)
- [Octopress](http://octopress.org/)
- [Learning Jekyll By Example: Build a Jekyll Website, Start to Finish | Andrew Munsell](http://www.andrewmunsell.com/tutorials/jekyll-by-example/index.html)
- [Archives in Jekyll - mitsake](http://www.mitsake.net/2012/04/archives-in-jekyll/)
- [Jekyll/Liquid Templating: How to group blog posts by year? - Stack Overflow](http://stackoverflow.com/questions/19086284/jekyll-liquid-templating-how-to-group-blog-posts-by-year?rq=1)
- [A week of symfony #351 (16->22 September 2013) - Symfony](http://symfony.com/blog/a-week-of-symfony-351-16-22-september-2013)
- [nirvdrum/svn2git](https://github.com/nirvdrum/svn2git)
- [String](http://caml.inria.fr/pub/docs/manual-ocaml/libref/String.html)
- [Unix system programming in OCaml](http://ocamlunix.forge.ocamlcore.org/)
- [Unix](http://caml.inria.fr/pub/docs/manual-ocaml/libref/Unix.html#TYPEopen_flag)
- [OCaml Journal: The Essence of Functional Programming](file:///home/jc/work/project/ocaml/ocaml-journal/www.ffconsultancy.com/products/ocaml_journal/subscribers/essence.html)
- [OCaml Journal: Implementing a simple XML-RPC client and server](file:///home/jc/work/project/ocaml/ocaml-journal/www.ffconsultancy.com/products/ocaml_journal/subscribers/xmlrpc.html)
- [Objective CAML Tutorial](http://mirror.ocamlcore.org/ocaml-tutorial.org/)
- [Open Source @ Jane Street](http://janestreet.github.io/)
- [OCaml :: 99 Problems (solved) in OCaml](http://ocaml.org/tutorials/99problems.html)
- [OCaml :: Tutorials](http://ocaml.org/tutorials/)
- [PLEAC-Objective CAML](http://pleac.sourceforge.net/pleac_ocaml/)
- [The Caml Hump: General purpose libraries :: Lexing and parsing](http://caml.inria.fr/cgi-bin/hump.en.cgi?sort=0&browse=96)
- [The Caml Hump: Ragel](http://caml.inria.fr/cgi-bin/hump.en.cgi?contrib=771)
- [Stream parser with Ragel and Ruby [Brighter Planet's Safety in Numbers]](http://numbers.brighterplanet.com/2011/06/14/stream_parser_with_ragel_and_ruby/)
- [A simple intro to writing a lexer with Ragel.](http://thingsaaronmade.com/blog/a-simple-intro-to-writing-a-lexer-with-ragel.html)
- [Adjustable type definitions for data exchange](http://mjambon.com/atd-biniou-intro.html)
- [Debian -- Package Search Results -- ocaml](http://packages.debian.org/search?keywords=ocaml&searchon=all&suite=testing&section=all)
- [utop/README.md at master · diml/utop](https://github.com/diml/utop/blob/master/README.md)
- [zed/src/zed_edit.ml at master · diml/zed](https://github.com/diml/zed/blob/master/src/zed_edit.ml)
- [Eliom](http://ocsigen.org/eliom/)
- [Ocsigen Tutorial](https://ocsigen.org/tutorial/application)
- [TyXML](https://ocsigen.org/tyxml/api/Html5.F)
- [core/lib/command.ml at master · janestreet/core](https://github.com/janestreet/core/blob/master/lib/command.ml)

