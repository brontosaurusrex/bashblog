---
title: compile inkscape (0.48.4) on wheezy from tarbal
author: bronto saurus
layout: post
permalink: /2013/12/compile-inkscape-on-wheezy-from-tarbal/
categories:
  - Uncategorized
---
<pre>2006  ./configure
 2007  sudo  apt-get build-dep inkscape
 2008  sudo apt-get install build-essential dpkg-dev fakeroot
 2011  ./configure 
 2013  make
 2016  sudo make install
 2017  inkscape &#038;</pre>

p.s. Make sure deb-src is enabled in /etc/apt/sources.list