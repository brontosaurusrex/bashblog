---
title: allow wordpress web updates
author: bronto saurus
layout: post
permalink: /2014/03/allow-wordpress-web-updates/
categories:
  - Uncategorized
---
Basically all wp files must be owned by the process running the wp, this did the trick for me;

<pre>sudo chown -R www-user:www-user ./</pre>

Then go to your wp-admin and run the updates &#8230;