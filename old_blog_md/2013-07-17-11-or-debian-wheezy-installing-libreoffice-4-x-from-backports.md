---
title: '#! 11 (or debian wheezy), installing libreoffice 4.x from backports'
author: bronto saurus
layout: post
permalink: /2013/07/11-or-debian-wheezy-installing-libreoffice-4-x-from-backports/
categories:
  - Uncategorized
---
<pre>sudo geany /etc/apt/sources.list</pre>

add

<pre>## b backports, only interested in libre office upgrades
deb http://http.debian.net/debian wheezy-backports main</pre>

run

<pre>sudo apt-get -t wheezy-backports install libreoffice</pre>

if it looks ugly, try

<pre>sudo apt-get install libreoffice-gnome libreoffice-gtk</pre>