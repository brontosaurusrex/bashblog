---
title: 'ffmpeg 23,976 > 25fps conversion'
author: bronto saurus
layout: post
permalink: /2014/09/ffmpeg-23976-25fps-conversion/
categories:
  - Uncategorized
---
ffmpeg

<pre>ffmpeg -r "25" -i "in.mov" -filter:a "atempo=1.0427" "out.mov"</pre>

which is probably similar to this avisynth (only the pitch is corrected as well);

<pre>AssumeFPS(25, 1, true)                 # Convert frame rate to PAL, also adjust audio.
SSRC(48000)                            # Restore audio sample rate to a standard rate.</pre>