---
title: mpv custom icon on Debian
author: bronto saurus
layout: post
permalink: /2014/01/mpv-custom-icon-on-debian/
categories:
  - Uncategorized
---
in /usr/share/applications make a file named mpv.desktop with following features;

<pre>[Desktop Entry]
Encoding=UTF-8
Type=Application
Exec=~/bin/mpv %F
Name=play
Icon=play
</pre>

& your icon theme must have that play.png or similar.