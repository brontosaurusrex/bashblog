---
title: vbox share host folder with guest
author: bronto saurus
layout: post
permalink: /2014/11/vbox-share-host-folder-with-guest/
categories:
  - Uncategorized
---
<pre>sudo mount -t vboxsf -o rw,uid=1000,gid=1000 share ~/host</pre>

where share is actual share name.

more: <https://forums.virtualbox.org/viewtopic.php?t=15868>