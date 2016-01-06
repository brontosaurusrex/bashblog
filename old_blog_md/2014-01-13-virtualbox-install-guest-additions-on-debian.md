---
title: virtualbox, install guest additions on Debian
author: bronto saurus
layout: post
permalink: /2014/01/virtualbox-install-guest-additions-on-debian/
categories:
  - Uncategorized
---
Follow these steps to install the Guest Additions on your Debian virtual machine:  
Login as root;  
Update your APT database with apt-get update;  
Install the latest security updates with apt-get upgrade;  
Install required packages with apt-get install build-essential module-assistant;  
Configure your system for building kernel modules by running m-a prepare;  
Click on Install Guest Additions… from the Devices menu, then run mount /media/cdrom.  
Run sh /media/cdrom/VBoxLinuxAdditions.run, and follow the instructions on screen.

from;

http://virtualboxes.org/doc/installing-guest-additions-on-debian/