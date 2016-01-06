---
title: ffmpeg mxf to png mov (ignore audio)
author: bronto saurus
layout: post
permalink: /2010/05/ffmpeg-mxf-to-png-mov-ignore-audio/
categories:
  - Uncategorized
---
`ffmpeg -i C0002.MXF -an -vcodec png C0002.mov`  
-an stands for ignore audio as it seems

examples of ffmpeg usage:  
<http://linuxnut.org/2009/01/ffmpeg/>