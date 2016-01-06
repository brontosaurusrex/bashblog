---
title: ubuntu replaygain idea
author: bronto saurus
layout: post
permalink: /2010/11/ubuntu-replaygain-idea/
categories:
  - Uncategorized
---
1. php uploader,  
allows wav?

2. refuse files longer than 1 minute?

3. encode wav to flac with  
`flac --replay-gain file.wav`

4. get the rg info and display that on page;  
`metaflac --list $file | grep REFERENCE | cut -d':' -f2`  
`metaflac --list $file | grep TRACK_GAIN | cut -d':' -f2`