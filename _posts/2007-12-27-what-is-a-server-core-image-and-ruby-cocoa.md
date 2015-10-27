---
ID: 695
post_title: 'what is a server? &#8230;Core Image and Ruby Cocoa!'
author: David
post_date: 2007-12-27 19:19:44
post_excerpt: ""
layout: post
permalink: >
  https://davidawindham.com/what-is-a-server-core-image-and-ruby-cocoa/
published: true
---
<object width="625" height="473"><param name="movie" value="http://www.youtube.com/v/jxhnWx_F69U&rel=1&border=1"></param><param name="wmode" value="transparent"></param><embed src="http://www.youtube.com/v/jxhnWx_F69U&rel=1&border=1" type="application/x-shockwave-flash" wmode="transparent" width="600" height="460"></embed></object>
I recently got an email with a simple question "what is a server?".. so in the most simple terms a server is just another computer just like your desktop that is networked to the "web". I like to call it your public computer vs your private computer..and your public computer (server) can store and retrieve (serve) all kinds of documents, images, media, and information. It is running an operating system that is a variant of unix.  And essentially you can connect to the remote computer and create and move files.  This is very simple when it comes to publishing html pages but can get very complex quickly when scripting languages are used to manipulate data in various methods using the hardware resources of your server.  In fact, search engine robots (another day :)) index pages in a very simple manner in much the way that antique browsers did like the lynx browser below.
<a href="http://en.wikipedia.org/wiki/Lynx_(web_browser)"><img src="http://davidawindham.com/images/lynx.png" alt="lynx browser" /></a>
The trick to serving up web pages and web enabled applications is mainly done with<a href="http://www.apache.org/"> Apache </a> (or another server) and it's modules which enable http request and various scripting languages.  What you see is a product of your browser interpreting this text sometimes with the help of plugins like javascript and flash.  The content of a site is served up in various ways.  I can't answer it all about the web in one post... <a href="http://en.wikipedia.org/wiki/WorldWideWeb">this is a good place to start</a>.. it was born on Christmas Day 1990...or if you would prefer the <a href="http://browsers.evolt.org/?worldwideweb/NeXT"> original files of the first internet browser</a>...When someone says content management, user generated content or dynamic content.. they generally mean content that can be edited and stored in a database.  In the most simple terms a database is like a big excel speadsheet hosted on your server, be it oracle, postgres, berkleydb or mysql... with tables and columns.  That data can be called upon by various scripting languages to appear in page or application.  Content management systems like typo, live journal, wordpress, joomla, drupal, moveabletype etc etc..
are just packages of scripts that give the average user ways to edit and manage this content with a simple user interface.  The advantages of using these systems is that you can generate custom dynamic content tools quickly by modifying the files and having a community of developers and pre-written code. The web is an ever evolving and you want your public server to be able to change with your needs.. and you want to be able to change it easily without upgrading hosting or web development companies. In order for us computer guys to keep everything up to date.. you've got to keep a local machine up to date with the latest stable releases of scripting languages, frameworks and apps...  these tools are what i recommend..  <a href="http://macromates.com/">Textmate </a> ,  <a href="http://www.bresink.com/osx/TinkerTool.html">Tinkertool </a>,  <a href="http://en.wikipedia.org/wiki/Command_line_interface">a Terminal</a>, and <a href="http://www.macports.org/">Macports </a>
<img src="http://davidawindham.com/images/tinker.png" alt="tinker tool" /><img src="http://davidawindham.com/images/macports.png" alt="mac ports" />
...add these  (<a href="http://macrabbit.com/cssedit/">CssEdit</a>, <a href="http://www.adobe.com/products/creativesuite/">CS3</a>, <a href="http://www.navicat.com/">Navicat</a>, <a href="http://cocoamysql.sourceforge.net/">Cocoa Sql</a>, <a href="http://www.eclipse.org/">Eclipse</a>) and that's about all i use.
And while plugins like Pulse and Aptana for Eclipse.. setting up workspaces is cake, but you'll never really learn to configure on your own... and I knew <a href="http://www.aptana.com/">aptana </a>was up to something.. it's now $99 and i'm sure pulse will follow.
<img src="http://davidawindham.com/images/pulse3.png" alt="pulse" />
<img src="http://davidawindham.com/images/jrails.png" alt="jrails aptana" />
Today, i was working with <a href="http://drupal.org/">Drupal 5.whatever</a> to see if i could use it in with wildcard domains.  I've noticed that several companies that need freelance work done are using it extensively so I picked up the most recent version and <a href="http://acquia.com/node/10">caught on to this concept</a> quickly after looking over the packages...  askimet (aka <a href="http://automattic.com/">Automattic</a>) is primarily fighting spam and looks like <a href="http://acquia.com/">Acquia</a> will be providing all kinds of $$ services for Drupal.  It just comes down to personal preference and I still like wordpress because it's familiar.. for most publishing projects add the multi-user version and <a href="http://bbpress.org/documentation/integration-with-wordpress/"> BB Press</a> with <a href="https://www.google.com/a/">Google Apps</a> / and or <a href="http://www.basecamphq.com/">Basecamp</a> and you've got something to work with? ... <a href="http://acquia.com/node/10">and $7 million</a>.. who knows what they'll do with it.. I think they should give it away...but what do i know about venture capital?
In doing so..(upgrading my local version of Drupal) i ended up working on my php install for quite some time... it was about time to upgrade
<img src="http://davidawindham.com/images/php.png" alt="php" /><img src="http://davidawindham.com/images/php2.png" alt="php two" />
and this is what i've found is a good way to do it..
<a href="http://www.entropy.ch/software/macosx/php/">it's a prebuilt package..from Mark Liyanage</a>
And..this is a great post from <a href="http://redartisan.com/2007/12/12/attachment-fu-with-core-image">Red Artisian</a> and they recently included the performance <a href="http://redartisan.com/blog">benchmarks of core image<img src="http://davidawindham.com/images/average.jpg" alt="core image" /></a>
And.. of note if you upgraded your rails to 2.0 <a href="http://weblog.rubyonrails.org/2007/12/17/rails-2-0-2-some-new-defaults-and-a-few-fixes">sqlite3 is now the default database</a> as this is standard in the leopard install
ps...I would like to thank santa clause for my new reads.
<img src="http://davidawindham.com/images/as3.png" alt="as3" /><img src="http://davidawindham.com/images/textmate.png" alt="textmate" />
and I would also like to thank The <a href="http://www.pragprog.com/">Pragmatic Bookshelf</a> for my updated versions.
<img src="http://davidawindham.com/images/pragmatic.png" alt="pragmatic" />
which has certainly helped with this..
<img src="http://davidawindham.com/images/rails2.png" alt="rails 2" />