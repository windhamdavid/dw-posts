---
ID: 727
post_title: 'Harbourtowne &#8211; 30th Anniversary'
author: David
post_date: 2008-03-12 08:05:48
post_excerpt: ""
layout: post
permalink: >
  https://macs.local/david/harbourtowne-30th-anniversary/
published: true
---
<img src="http://davidawindham.com/images/hbr_web.png" alt="harbourtowne real estate" />

   Fudgy Brabham, the broker in Charge of Harbourtowne and Trident Real Estate is celebrating thirty years this year.  Fudgy and I have mulled over the impact of the internet to real estate in the last three years.  I met Fudgy through my <a href="http://leowindham.com">father</a> four years back when I was getting my license from CTAR in order to download data about real estate for other websites and subsequently have had my license with him since.  He is a 'larger' than life man.. with great ideas about politics, cooking, people, and novels.  I began doing <a href="http://charlestonhometour.com">home tours</a> for real estate several years back with the spinning pictures and all  :)... video, maps and all that good stuff.  I burned out doing it fairly quickly but since then.. i've had some solid opinions about marketing properties online.  It's simple.. get your listing to look as good as possible online and get it everywhere with your name on it and then point all of your other marketing collateral there too.  So we (<a href="http://weblog.commandlinejunkie.com">kris</a> and i) began <a href="http://www.windhambrothers.com/syndicate.htm">syndicating</a> real estate listing data for brokerages using a bit of rb, php, sql, and <a href="http://base.google.com/">google base</a>... we'll, recently Fudgy and I went over the common misconceptions and problems that agents have with online marketing and I decided to see if I couldn't tackle those for his agency.

1) email.. how do i manage 100+ email accounts (easy dependable and inexpensively)
2) website.. how do i manage a website (easy dependable and inexpensively) without learning to use software.. how do i add/edit pages what do i do with my current hosting and domains?
3) some agents want to use their own websites and listing pages.. do they work? who should do them? single property websites? virtual tours? email blast?

and voila... case study #2 in two weeks.

the answers
1) email..  for any size company... unless you have your own IT guys to troubleshoot and admin email accounts on your own properly configured servers with backup recovery .. don't be dependent on some third party web hosting company who is likely dependent on another party.. ie the hosting company who admins their servers to handle your email accounts.. and while godaddy and other hosting domain companies are fine as an email host, your ISP (internet service provider) is also fine (although i find comcast, time warner and the like spammy... and what do you do when you want to switch service providers.. give up your email?)  so here's what i find works well.. I move all the dns records to google apps for domains.  This solves all of those problems... it's mobile, plays well with crackberries, it's spam resistant and it's easy, cheap, and dependable... and now they've added backup recovery from postini for the larger (legal, medical, .edu) outfits..

<img src="http://davidawindham.com/images/hbr_login.png" alt="login" />
<img src="http://davidawindham.com/images/hbr_dns2.png" alt="dns" />
<img src="http://davidawindham.com/images/hbrtwn_email.png" alt="email" />

2)Fudgy had been using microsoft frontpage and his home brewed copy and paste html skills to edit the roster and listings online.  He told me that quite frankly he wanted to spend less time doing this.. so what i did is make it so that he can import or export excel spreadsheets for his roster pages and he can copy and paste listings from ctar onto his listing pages.  With Wordpress controlling/editing/adding images and all that jazz isn't in code.. it's copy and paste.. and expanding or adding pages and features to the site doesn't require a web development company.. just a couple minutes of his time.

3)agent website stuff... there are a bunch of pre-fab ways to market online.. but let's face it.. every brokerage and agent wants them leading back to their domain, url, name and logo and sending clients to www.thissite.com/somepage/someotherpage/ect.com isn't a good practice, even though sometimes these places can work for you like google base, oodle, craigslist and vflyer... they will generate spam to your email and you should want those places generating traffic for your site and not vice versa..

so here is what i did (don't try this at home unless you add all of the proper precautions).. i put in a <a href="http://mu.wordpress.org/">multi user wordpress</a> install on a grid server at <a href="http://mediatemple.net/go/order/?refdom=windhambrothers.com">media temple</a>.. i customized the back and front end, removed the bulky features, removed the wp-signup.php for security and spam reasons, added a bunch of security measures and only allowed users will emails from @hbrtwn.com, put a single sign on service to the google apps, gave every agent their own websites to control  http://name.hbrtwn.com and added enough functionality so that listings can be copied and pasted into pages from ctar, galleries of images can be uploaded and put onto and page... and began a <a href="http://david.hbrtwn.com">training page</a> to teach all of these folks to use the site.

**the best part about a multi user site instead of individual sites is that everyone who works with their webpages will actually benefit everyone else in the group search engine-wise..

and ps... i took all of the images excepting one <a href="http://hbrtwn.com">http://hbrtwn.com</a> (a friend of fudgy's took the shem creek at dusk images)

<img src="http://davidawindham.com/images/hbr_wpapps.png" alt="wpapps" />
<img src="http://davidawindham.com/images/hbr_mice.png" alt="wysiwyg" />

The Result:
<a href="http://hbrtwn.com">www.hbrtwn.com</a>
Timeline:  - exactly one week start to finish.. email addresses were up and down with no lag time or lost email. Every agent gets their own website that they can design with all the bells and whistles and multiple email addresses with less spam.. and Fudgy can spend less time on his computer.
Price: 40hrs x $35/hr ($1400)