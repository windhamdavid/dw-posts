---
ID: 696
post_title: >
  Apache 2 PHP 5 and MySql 5 on Tiger
  10.4.11
author: David
post_date: 2007-12-30 10:54:20
post_excerpt: ""
layout: post
permalink: >
  https://macs.local/david/apache-2-php-5-and-mysql-5/
published: true
---
It took some tinkering.. but it's done... and it's not for the faint at heart.
Don't go with the prefab installers... build it all from source, and <strong>be forewarned</strong> that it is easy to develop conflicts with an existing apache 1.3 install on a mac..
...please <strong>back up</strong> your disk and os before you start.. I recovered twice while i was upgrading.  These <a href="http://www.phpmac.com/articles.php?view=237">tutorials are helpful</a> .... <a href="http://rubypond.com/articles/2007/08/27/installing-apache-2-2-4/">and another</a>  and you'll want <a href="http://www.modpython.org/">mod python</a> if you <a href="http://www.djangoproject.com/documentation/modpython/">want to run Django</a> which requires at least <a href="http://www.python.org/">Python 2.x</a> and <a href="http://httpd.apache.org/docs/2.2/">Apache 2.x</a>... and i might as well <a href="http://www.lighttpd.net/">update <a href="http://www.lighttpd.net/">Lighttpd </a>while i'm at it, b/c serving media is better with it using <a href="http://www.modpython.org/">mod python</a>.
<img src="http://davidawindham.com/images/lighttpd.png" alt="lighttpd" />
<img src="http://davidawindham.com/images/python.png" alt="python" />
<img src="http://davidawindham.com/images/php3.png" alt="php 5" />
<img src="http://davidawindham.com/images/apache_config.png" alt="apache config" />
<img src="http://davidawindham.com/images/php_admin.png" alt="php admin" />
no need for leopard now... excepting maybe time machine but i think <a href="http://www.bombich.com/software/ccc.html">carbon copy cloner</a> works well.
<img src="http://davidawindham.com/images/carbon.png" alt="carbon copy cloner" />
