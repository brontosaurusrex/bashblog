---
title: compile plank 0.6 on wheezy
author: bronto saurus
layout: post
permalink: /2014/05/compile-plank-0-6-on-wheezy/
categories:
  - Uncategorized
---
get the 0.6 tarball , extract, ect

sudo apt-get install automake gnome-common intltool pkg-config valac libbamf3-dev libdbusmenu-gtk3-dev libgdk-pixbuf2.0-dev libgee-dev libglib2.0-dev libgtk-3-dev libwnck-3-dev libx11-dev 

./configure

make

sudo make install