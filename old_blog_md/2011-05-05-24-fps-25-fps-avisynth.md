---
title: '24 fps > 25 fps avisynth'
author: bronto saurus
layout: post
permalink: /2011/05/24-fps-25-fps-avisynth/
categories:
  - Uncategorized
---
<pre lang="avisynth">AssumeFPS(25, 1, true)                 # Convert frame rate to PAL, also adjust audio.
SSRC(48000)                            # Restore audio sample rate to a standard rate.</pre>