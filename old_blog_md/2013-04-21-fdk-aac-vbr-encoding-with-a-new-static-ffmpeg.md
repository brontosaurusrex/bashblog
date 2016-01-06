---
title: fdk-aac vbr encoding with a new static ffmpeg
author: bronto saurus
layout: post
permalink: /2013/04/fdk-aac-vbr-encoding-with-a-new-static-ffmpeg/
categories:
  - Uncategorized
---
`ffmpeg -i input.mp4 -c:v copy -c:a libfdk_aac -vbr 3 output.mp4`