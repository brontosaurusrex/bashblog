---
title: radio ga-ga, get latest link from xml
author: bronto saurus
layout: post
permalink: /2013/11/radio-ga-ga-get-latest-link-from-xml/
categories:
  - Uncategorized
---
<pre>curl http://www.rtvslo.si/podcasts/radio_gaga.xml | grep -m 1 mp3 | cut -d\" -f 6</pre>

or to play

<pre>mpv `curl http://www.rtvslo.si/podcasts/radio_gaga.xml | grep -m 1 mp3 | cut -d\" -f 6`</pre>

(gaga)  
or  
<http://paste.debian.net/plain/107554>