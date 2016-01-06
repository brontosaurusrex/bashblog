---
title: flac to lossy flac (via lossyway)
author: bronto saurus
layout: post
permalink: /2008/07/flac-to-lossy-flac-via-lossyway/
categories:
  - audio, software
---
flac -d thisflac.flac &#8211;stdout &#8211;silent|lossywav &#8211; &#8211;stdout|flac &#8211; -b 512 -othisflac.lossy.flac &#8211;silent