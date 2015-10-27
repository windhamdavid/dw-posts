---
ID: 718
post_title: audiovisual actionscript
author: David
post_date: 2008-02-22 15:23:44
post_excerpt: ""
layout: post
permalink: >
  https://davidawindham.com/audiovisual-actionscript/
published: true
---
<a href="http://code.google.com/p/popforge/"><img src="http://davidawindham.com/images/popforge.png" alt="popforge" /></a>
Popforge is an Actionscript 3 code sandbox started by <a href="http://void.andre-michelle.com/">Andre Michelle</a> and <a href="http://je2050.de/">Joa Ebert</a>.... it's hosted at <a href="http://code.google.com/p/popforge/">google code</a>.... they did the roland909 and <a href="http://8bitboy.popforge.de/">8bitboy</a> - the amiga sound emulator....
<a href="http://live.popforge.de/"><img src="http://davidawindham.com/images/909.jpg" alt="roland909" /></a>
and they've also got this <a href="http://cubicvr.popforge.de/">great cubic vr processor</a> for flashplayer9... and it's one of the very few free non javascript dependent vr scripts..nice work all around... and they've got something to do with hobnox which looks like some serious business.
<a href="http://us.hobnox.com/index.542.html"><img src="http://davidawindham.com/images/hobnox.jpg" alt="hobnox" /></a>
<img src="http://davidawindham.com/images/mi145.jpg" alt="mi145" />
[kml_flashembed movie="http://davidawindham.com/org/first.swf" height="550" width="800" /]
speaking of digital audio.. that's a composition written and played by my <a href="http://weblog.commandlinejunkie.com/">bro</a> you're listening to.
<pre lang="actionscript" lineno="1">
var s:Sound = new Sound();
var sc:SoundChannel;
var ba:ByteArray = new ByteArray();
var array:Array;
s.load(new URLRequest("jazz_sax.mp3"));
sc = s.play(0,1000);
this.addEventListener(Event.ENTER_FRAME, spectrum);
var a:Number = 0;
function spectrum(event:Event)
	{ a = 0;

	graphics.clear();

    SoundMixer.computeSpectrum(ba,true,0);

    for(var i=0; i < 556; i=i+3)

    {

    a = ba.readFloat();

    var num:Number = a*360;

    graphics.lineStyle(num/19,0x999999|(num << 5));

    graphics.drawCircle(stage.stageWidth/2.5,stage.stageHeight/2.5,i);

              }

              }
</pre>