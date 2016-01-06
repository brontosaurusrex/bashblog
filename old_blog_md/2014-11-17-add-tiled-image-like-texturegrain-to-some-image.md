---
title: '#! add tiled image (like texture/grain) to some image'
author: bronto saurus
layout: post
permalink: /2014/11/add-tiled-image-like-texturegrain-to-some-image/
categories:
  - Uncategorized
---
<pre>convert input_1280x1024.png -background none -size 1280x1024 tile:/path/to/default-tile.png -composite out_1280x1024.png</pre>