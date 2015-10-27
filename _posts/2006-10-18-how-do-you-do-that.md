---
ID: 592
post_title: how do you do that?
author: David
post_date: 2006-10-18 14:57:04
post_excerpt: ""
layout: post
permalink: >
  https://macs.local/david/how-do-you-do-that/
published: true
---
for the most part, google, yahoo, live.com, ask.com, search.com, msn etc...
use an algorithm like the <a href="http://en.wikipedia.org/wiki/PageRank">page rank system</a> which is patented by Google.
<a href="http://www-db.stanford.edu/~backrub/google.html">the paper that started it all... check out the pics!</a>
<a href="http://patft.uspto.gov/netacgi/nph-Parser?Sect1=PTO1&Sect2=HITOFF&d=PALL&p=1&u=%2Fnetahtml%2FPTO%2Fsrchnum.htm&r=1&f=G&l=50&s1=6,285,999.PN.&OS=PN/6,285,999&RS=PN/6,285,999">
US Patent 6285999</a>
It's some heavy stuff....
but I'll try it in thirty words or less.

<a href="http://en.wikipedia.org/wiki/Sergey_Brin">Sergey Brin (Сергей Михайлович Брин)</a> and <a href="http://en.wikipedia.org/wiki/Larry_Page">Larry Page </a>(both 33, founders of google, the 26th and 27th richest people in the world according to Forbes ) created page rank while at school..
ok.. that doesn't count for my thirty words..
Searches are based on <a href="http://en.wikipedia.org/wiki/Probability_distribution"> Probability Distribution</a> which are alot like the ole bell curve in class.. you assign every number (grade) a probabilty and you use functions for a distribution graph like this beta distribution
<img src="http://davidawindham.com/images/betadistribution.gif" alt="Beta Distribution Graph" / width="425" height="350">
In trying to match terms with pages, it gives each page a ranking which is updated everytime the site is crawled.  The ranking is determined by a series of algorithms that try to determine link probablilty in the distribution. <img src="http://davidawindham.com/images/equation.gif" alt="Alorithm" />
That's PR (page ranking) N (number of pages) L (links) d(dampening factor) M(pages that link to the page) (p) (other pages under consideration for ranking)   got it?
The damponing factor determines that any random internet surfer will eventually stop clicking!
If you really want to know more...  here you go..
<a href="http://en.wikipedia.org/wiki/Modified_adjacency_matrix">Modified Adjacendy Matrix</a>
<a href="http://en.wikipedia.org/wiki/Markov_chain">Markov Chain</a>
<a href="http://en.wikipedia.org/wiki/Eigenvector_centrality">Eigenvector Centrality</a>

There are ways to spoof the formulas, but the best long term approach is to give straightfoward content  as it closely pertains to your site, use xml sitemaps, maintain standards complient code, update content often, use rss, but most of all don't over do anything... the mathmatics behind the search engines are very democratic and straightfoward content is the easiest way to achieve results... and if this doesn't work, you can always go giving the guys at google or some other middleman "SEO guru" more money for paid placement. :)

<a href="http://www.googleduel.com/original.php">I like googleDuel</a> and google analytics for figuring out search habits.