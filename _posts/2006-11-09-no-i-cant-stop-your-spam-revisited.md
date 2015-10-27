---
ID: 595
post_title: '.. no I can&#8217;t stop your spam revisited.'
author: David
post_date: 2006-11-09 23:12:58
post_excerpt: ""
layout: post
permalink: >
  https://macs.local/david/no-i-cant-stop-your-spam-revisited/
published: true
---
*   Spam (R) (capitalized) is a registered trademark of a meat
       product made by Hormel. Use of the term spam (uncapitalized) in
       the Internet community comes from a Monty Python sketch and is
       almost Internet folklore. The term spam is usually pejorative,
       however this is not in any way intended to describe the Hormel
       product.
the more I talk computers, the more I hear spam.. client after client..
and this is the primary reason I don't run any client emails through our servers.
They are better served by an ISP or hosting provider with 24/7 support and I don't have to deal with the security risk associated with qmail.
I began recieving some strange notices from one of my servers last week and after a good look at the <a href="http://www.vpsland.com">server</a>, we discovered some issues with security, qmail, and smtp..
so here's my quick advice and some further reading material.. .... most spam originates from a <a href="http://www.spamhaus.org/rokso/index.lasso">small number of outfits</a>, and ever since the <a href="http://www.ftc.gov/bcp/conline/pubs/buspubs/canspam.htm">
Cam Spam act of 2003</a> gave some bite to laws against unsolicited email, most of these outfits try to conceal thier identities by relaying, using small ISP's etc..
this is what I say, if you maintain a server or an entire network, you should feel obligated to make sure that it is secure for the benefit of everyone.  And my advice to anyone who recieves spam.  <a href="http://www.ftc.gov/spam/">Report it here</a> and don't publish an email address unless absolutely nessesary...
<a href="http://www.saout.de/misc/spf/">SPF for Qmail</a>
<a href="http://www.openspf.org/">Sender Policy Framework</a>
<a href="http://new.openspf.org/Introduction">SPF Introduction</a>
<a href="http://cr.yp.to/qmail.html">Qmail</a>
<a href="http://esmtp.sourceforge.net/">eSMTP</a>
<a href="http://cr.yp.to/smtp.html">SMTP</a>
<a href="http://en.wikipedia.org/wiki/Simple_Mail_Transfer_Protocol">SMTP Introduction</a>
<a href="http://tools.ietf.org/html/rfc2821">SMTP detailed</a>
<a href="http://tools.ietf.org/html/rfc2505">Anti-Spam Recommendations for SMTP MTAs</a>
<a href="http://en.wikipedia.org/wiki/IMAP">IMAP</a>
<a href="http://en.wikipedia.org/wiki/Post_Office_Protocol">POP (post office protocol)</a>
<a href="http://en.wikipedia.org/wiki/Comparison_of_e-mail_clients">Compare Email Clients</a>
<a href="http://www.spamhaus.org/statistics/spammers.lasso">Most Wanted</a>
<a href="http://www.spamhaus.org/statistics/networks.lasso">Worst Networks</a>
