---
title: asus eee 1201n and lucid and bluetooth mice
author: bronto saurus
layout: post
permalink: /2010/06/asus-eee-1201n-and-lucid-and-bluetooth-mice/
categories:
  - Uncategorized
---
[<img src="http://brontosaurusrex.69.mu/wp-content/uploads/2010/06/mouse.jpg" alt="bluetooth mice" title="mouse" width="140" height="240" class="alignleft size-full wp-image-922" />][1]  
1. instal blueman (bluetooth manager)  
2. see if that works  
3. if after reboot things wont connect or you get bluez daemon not running, try:  
sudo /etc/init.d/bluetooth start  
4. try to add the same into your startup apps  
/etc/init.d/bluetooth start

 [1]: http://brontosaurusrex.69.mu/wp-content/uploads/2010/06/mouse.jpg