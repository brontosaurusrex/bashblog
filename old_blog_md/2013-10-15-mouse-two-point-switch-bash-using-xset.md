---
title: Mouse two-point switch / bash (using xset)
author: bronto saurus
layout: post
permalink: /2013/10/mouse-two-point-switch-bash-using-xset/
categories:
  - Uncategorized
---
<pre>#!/bin/bash

# This is a little 2-point mice behaviour switch
# Thanks to &lt;emg> from freenode/#bash for the awk line.

# install:
# copy to ~/bin as mice, then "chmod +x mice"

if xset q | awk '/acc/{if($2=="2/1" &#038;&#038; $4=="4")exit(0);exit(1)}'

then 
# put your settings here
xset m 1/3 1
echo "Mice custom settings active"
else 
# back to system defaults
xset m default
echo "Mice system defaults active"
fi
xset q | grep acc</pre>