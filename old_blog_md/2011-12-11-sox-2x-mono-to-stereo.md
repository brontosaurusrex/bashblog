---
title: sox 2x mono to stereo
author: bronto saurus
layout: post
permalink: /2011/12/sox-2x-mono-to-stereo/
categories:
  - Uncategorized
---
https://www.nesono.com/node/275

The following command merges the two mono files into one stereo WAV file (order: left, right):

`sox -M input.l.wav input.r.wav output.wav`

not tested