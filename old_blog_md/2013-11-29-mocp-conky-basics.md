---
title: mocp conky basics
author: bronto saurus
layout: post
permalink: /2013/11/mocp-conky-basics/
categories:
  - Uncategorized
---
<pre>color0 000000
color1 999999
##############################################
#  Output
##############################################
TEXT
${font URW Gothic L:size=27}${color1}${execi 10 mocp -Q %song}${color0}${font URW Gothic L:size=17} 
${execi 10 mocp -Q %artist}
</pre>