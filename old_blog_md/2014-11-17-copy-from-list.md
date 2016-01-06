---
title: copy from list
author: bronto saurus
layout: post
permalink: /2014/11/copy-from-list/
categories:
  - Uncategorized
---
Copy files that are in files.txt in flat fashion to current dir;

<pre>rsync -avb --no-dirs --no-relative --files-from="files.txt" / ./</pre>