---
ID: 1290
post_title: Chrome Devtools Theme
author: David
post_date: 2015-01-28 13:31:27
post_excerpt: >
  After a recent Chrome update, I noticed
  that the elements tab in my development
  tools theme was no longer functioning
  and became a bit unreadable with the
  default styles.
layout: post
permalink: >
  https://davidawindham.com/chrome-devtools-theme/
published: true
meta-desc:
  - >
    After a recent Chrome update, I noticed
    that the elements tab in my development
    tools theme was no longer functioning
    and became a bit unreadable with the
    default styles.
---
After a recent Chrome update, I noticed that the elements tab in my development tools theme was no longer functioning and became a bit unreadable with the default styles.  This also happened a year or so ago as well when Chrome stopped supporting the custom css rules for the development tools web inspector. I use Chrome, Safari, and Mozilla developer tools and I think each have nice debugging and consoles, but I've always been particularly fond of Chrome because I keep it customized to match my other editor themes. I've flipped themes over the years. I started on Notepad++ using a dark theme because it seemed to mimic a terminal window. I read an article about halation and switched back to a white background. I migrated over to Textmate and started using the Sunburst theme and the Menlo font. I switched to Solarized when that came out. When I was watching Railscast, I switched to that theme. When Sublime Text first came out, I switched to Monokai. I started using Atom and switched to Base16 dark. However, I always seem to switch back to Sunburst with the Menlo monospaced font and have continued to use that theme in every editor I use. I'm not exactly sure what it is I like. It could be just habit at this point but I can say that the cool blues, mellow yellows and oranges fit me just right. 

So I had to publish an extension that hacked the theme back into my development tools element inspector. The hackety-hack is in the pseudo ::shadow elements in the canary.css and the Github repo is available at <a href="https://github.com/windhamdavid/sunburst-devtools">https://github.com/windhamdavid/sunburst-devtools</a>. The Google Chrome plugin is available at <a href="https://chrome.google.com/webstore/detail/devtools-theme-sunburst/fkigcimlehjhpnejpiohmibcidmobcpo">https://chrome.google.com/webstore/detail/devtools-theme-sunburst/fkigcimlehjhpnejpiohmibcidmobcpo</a>
&nbsp;
<img src="https://davidawindham.com/wp-content/uploads/2015/01/sunburst-screen-devtools.png" alt="Sunburst DevTools Theme" width="100%" class="alignnone size-full wp-image-1354" />