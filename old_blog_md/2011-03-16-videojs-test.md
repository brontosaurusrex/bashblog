---
title: videojs test
author: bronto saurus
layout: post
permalink: /2011/03/videojs-test/
categories:
  - Uncategorized
---
problems with implementation:  
&#8211; ugly default skin (just my opinion)  
&#8211; it doesn&#8217;t look the same in html5 and flash mode (i&#8217;d rather not have flash mode in that case at all) < bad default, wrong flash player  
&#8211; video is streched by default in flash mode, when it boxed in html5 mode (the correct way) < bad default  
&#8211; it doesnt provide any built-in means to embed size automagically, my php script does that for years now&#8230;  
&#8211; the url to video must be full, otherwise it will fail playback in flash mode < bad default, html5 version should have the same behaviour

html5 problems:  
&#8211; chrome on windows doesn&#8217;t seem to be any faster when decoding h.264 than flash  
&#8211; no fullscreen  
&#8211; the whole html5 idea suckors to the balls