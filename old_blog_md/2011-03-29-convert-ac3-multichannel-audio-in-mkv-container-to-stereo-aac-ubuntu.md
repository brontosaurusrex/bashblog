---
title: 'convert ac3 multichannel audio in mkv container to stereo AAC &#8211; ubuntu'
author: bronto saurus
layout: post
permalink: /2011/03/convert-ac3-multichannel-audio-in-mkv-container-to-stereo-aac-ubuntu/
categories:
  - Uncategorized
---
1. `ffmpeg -i muki.mkv -vn -acodec pcm_s16le -ac 2 muki.wav`  
2. `neroAacEnc -q 0.5 -if muki.wav -of muki.aac`  
(this can also be piped &#8211; a one step process)  
3. remux with mkvmerge GUI (or cli)

more: <http://wiki.flexion.org/ConvertingMKV.html#7.0>