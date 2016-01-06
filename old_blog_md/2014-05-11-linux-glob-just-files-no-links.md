---
title: linux, glob just files, no links
author: bronto saurus
layout: post
permalink: /2014/05/linux-glob-just-files-no-links/
categories:
  - Uncategorized
---
<pre>find . -maxdepth 1 -type f -print0 | xargs -0r yourCommand</pre>

or more precisely;

<pre>find . -type f -name "*.svg" -print0 | xargs -0r svgToBW</pre>