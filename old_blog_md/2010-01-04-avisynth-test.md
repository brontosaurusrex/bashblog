---
title: avisynth test
author: bronto saurus
layout: post
permalink: /2010/01/avisynth-test/
categories:
  - Uncategorized
---
<pre lang="avisynth" line="1"># directshowsource("R:5okt07_hd_Cineformtest2.avi")
directshowsource("R:5okt07_hd_Cineformtest.avi")
# b=wavsource("R:5okt07_hd_Cineformtest3.wav")

# RESIZING
LanczosResize(720,432)

# BORDERS
AddBorders(0,72,0,72)

converttoyv12()
</pre>