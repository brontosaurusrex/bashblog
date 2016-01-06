---
title: magic ubuntu 10.10 flash solver
author: bronto saurus
layout: post
permalink: /2011/03/magic-ubuntu-10-10-flash-solver/
categories:
  - Uncategorized
---
`sudo apt-get --purge remove swfdec-mozilla adobe-flashplugin browser-plugin-gnash gnash gnash-common mozilla-plugin-gnash swfdec-mozilla; sudo dpkg -P flashplugin-installer; sudo apt-get --purge autoremove; sudo apt-get clean; sudo apt-get -y install flashplugin-nonfree`

or for more gracefull approach run this first:  
`dpkg -l | grep flash; dpkg -l | grep gnash; dpkg -l | grep swf`