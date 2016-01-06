---
title: restrict ssh access to specific user
author: bronto saurus
layout: post
permalink: /2012/04/restrict-ssh-access-to-specific-user/
categories:
  - Uncategorized
---
You do this by adding a line like this to /etc/ssh/sshd_config

AllowUsers brontosaurus

then:  
service ssh restart