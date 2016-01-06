---
title: playonlinux install on wheezy
author: bronto saurus
layout: post
permalink: /2014/10/playonlinux-install-on-wheezy/
categories:
  - Uncategorized
---
<http://www.playonlinux.com/en/download.html>  
the addkey command should use sudo for the apt-key part;

<pre>wget -q "http://deb.playonlinux.com/public.gpg" -O- | sudo apt-key add -</pre>