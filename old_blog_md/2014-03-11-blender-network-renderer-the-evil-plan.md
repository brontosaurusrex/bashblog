---
title: Blender network renderer, the evil plan
author: bronto saurus
layout: post
permalink: /2014/03/blender-network-renderer-the-evil-plan/
categories:
  - Uncategorized
---
Client is a desktop machine (s)

Master and also Slave is one of the ssh servers (cli stuff).  
Slave is another ssh server.  
(So in any moment in time at least 2 slaves are rendering).

Clients can also be slaves, so overnight 4 machines could render (both desktops, both servers).

Find some other possible slaves?