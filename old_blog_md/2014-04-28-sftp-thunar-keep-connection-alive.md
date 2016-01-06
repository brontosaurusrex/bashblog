---
title: 'Sftp &#038; Thunar, keep connection alive'
author: bronto saurus
layout: post
permalink: /2014/04/sftp-thunar-keep-connection-alive/
categories:
  - Uncategorized
---
<http://crunchbang.org/forums/viewtopic.php?id=34161>

untested;  
*1) create file on your local machine:  
$ touch ~/.ssh/config  
2) put following in this file:  
Host *  
ServerAliveInterval 240*