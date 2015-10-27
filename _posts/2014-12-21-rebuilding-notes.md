---
ID: 1244
post_title: Notes on Rebuilding
author: David
post_date: 2014-12-21 19:18:39
post_excerpt: ""
layout: post
permalink: >
  https://davidawindham.com/rebuilding-notes/
published: true
meta-desc:
  - >
    Just some notes on rebuilding this
    website.
---
I've recently put a little bit of my holiday time into rebuilding this website. It's almost been online for ten years and I figured it could use a little overhaul. 

<a href="https://github.com/windhamdavid/dw" target="_blank">Here's the Git Repo</a> <a href="https://github.com/windhamdavid/dw"><span class="fa fa-15x fa-code-fork"></span> </a>

<h5>I'll just going to make some notes on it here:</h5>

I built a little video chat application that allows anyone to connect with me from my homepage. I've added a setting that allows me to set when I'm online. If that is set on, a small notification comes up on my home page that asks if the visitor would like to connect. If they press yes, I am sent a text message which appears on my phone and computer screens. The visitor is given a loading message while I get connected to the chat. I am using Node.js, Express, and WebRTC.io for the video chat application. I am using Twilio for the SMS notifications and the STUN server via <a href="https://www.twilio.com/blog/2014/12/set-phasers-to-stunturn-getting-started-with-webrtc-using-node-js-socket-io-and-twilios-nat-traversal-service.html" title="Twilio STUN Webrtc" target="_blank">this post</a>. Only Chrome and Firefox support it now, but it's only a matter of time before Safari and mobile browsers follow suit. I built a little API that counts the active connections and emits a JSON string. The website attempts to read this 5 times, 5 seconds apart. If I get connected, the visitor is connected. It's fun. My first chat was from a random visitor in Italy.  It's a bit like <a href="http://en.wikipedia.org/wiki/Chatroulette" title="Chatroulette" target="_blank">chat roulette</a> in that way. I'll add in form to ask who they are before I get sent the SMS later on. Twilio is so cheap I can't believe how much I pay for unlimited texting with AT&T... I might also route those through Twilio later on.  

<pre data-language="javascript">
function poll_dave() {
   var x = 0;
   var countTimer = setInterval(function() {
      if (x &gt; 5) { clearInterval(countTimer) }
      else if (x == 5) { dave_not_available() }
      else {
         var URLchatAPI = "http://macs.local:8080/status";
         var request = $.ajax({
            url: URLchatAPI,
            dataType: 'json',
            cache: false, 
            success: function (data) {
               online = data.online;
                  if (online=='yes') {
                     $('.chat').modal('show');
                     x = x+5;
                  };
                  if (online=='no') {
                     dave_connecting();
                  };
            },
            error: function ( xhr, tStatus, err ) {
               dave_error();
               x = x+5;
            }
         });
      x++;
      }
   }, 5000);
});</pre>

<h5>Third Party Dependence:</h5>
One of the main reasons I built the video chat was because I was tired of using my Google Apps accounts for chat and video chat. An in that same vein, I've also put in my own hosted analytics using <a href="http://piwik.org/" title="Piwik" target="_blank">Piwik</a>. Here is <a href="https://davidawindham.com/about/analytics" title="David Windham Analytics">public facing analytics page</a>.  It has a nice little mobile app too. I also try to use as little as possible third party code.  There are only three third party plugins running. I am using Gravity Forms, Mandrill for email, and Askimet for spam.  

<h5>Speeding it up:</h5>
I put some thought into migrating everything over to a static file system, Ghost or another Javascript based system. I kinda wanted to stay loyal to WordPress since this site started there. I did however built this theme to make use of the WP-API and Backbone which means that I could always add a new front end whenever I'm ready. The infinite scroll is powered by Backbone.  I'm sure that Socket.io is somewhere in the future since Automattic started maintaining it when they acquired CloudUp. I am also moving over to a Nginx and Redis cacheing system as I migrate to a new host. Even though my queries are tiny, I still find the half second lag pretty painful.  

<h5>ROI:</h5>
Since almost all of my work comes from direct referrals, it doesn't make a lot of sense to market myself. Because of that, I've had the luxury of really not paying any attention to my own website.  However, I have wanted to streamline some of my workflow and communications. And because of that, I've built a client billing and project management into this site. I am still using a clone of Basecamp called Project Pier, but I have now integrated that into the billing user management of this site. 

<h5>Actually Posting Content:</h5>
Much like I've just posted these notes, I'm gonna start posting other fun stuff online.  This may be a bad decision as it means that I'll be sharing these postings elsewhere. I rarely log into any social networks and I've found it helps simplify my attention and keeps my focus at home.  What really inspired me to do this was the fact that I've been reading all of the recent "Best Albums of 2014" from various publishers and I keep complaining to my better half about how bad they are and thinking to myself that I should post my own. So I built a page to keep up with all of the music I listen to at <a href="http://davidawindham.com/studio/music" title="David Windham Music Listening Habits">http://davidawindham.com/studio/music</a>
