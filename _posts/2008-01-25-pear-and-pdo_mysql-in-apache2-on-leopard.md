---
ID: 702
post_title: Pear and pdo_mysql in Apache2 on Leopard
author: David
post_date: 2008-01-25 11:13:44
post_excerpt: ""
layout: post
permalink: >
  https://macs.local/david/pear-and-pdo_mysql-in-apache2-on-leopard/
published: true
---
<img src="http://davidawindham.com/images/pdo_mysql.png" alt="pdo_mysql" />
seems to be a common issue with leopard's php install..folks are looking to add the modules for pdo_mysql and the pear libraries...  before you go reinstalling apache and rebuilding php5 from source.. and getting lost in Leopards symbolic links to the php.ini and httpd.conf files..like I did <a href="http://discussions.apple.com/thread.jspa?messageID=6437976">here..</a> using this <a href="http://www.entropy.ch/software/macosx/php/">PHP Apache Module</a> and it gets especially tricky if you are on a G5 with 64bit architecture... see this <a href="http://www.entropy.ch/phpbb2/viewtopic.php?p=10813">post</a> or <a href="http://reduxcomputing.com/leopard-php5.html">this one</a> or <a href="http://blog.bitxtender.com/post/23017941">this one.</a>
<img src="http://davidawindham.com/images/pearphp.png" alt="php" />
<img src="http://davidawindham.com/images/apacheconfig2.png" alt="apache errors" />