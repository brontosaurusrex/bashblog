---
title: '1280&#215;720 50p to pal 4:3 BFF interlaced, avisynth'
author: bronto saurus
layout: post
permalink: /2011/03/1280x720-50p-to-pal-43-interlace-avisynth/
categories:
  - Uncategorized
---
<pre lang="avisynth"># naloži plugin
LoadPlugin("t:utilityavisynthffmpegsourceFFMS2.dll")

# naloži video klip
a=ffaudiosource("F:folderfile.MOV")
v=ffvideosource("F:folderfile.MOV")
audiodub(v,a)

# pokropaj na sredino in resize (tu smo še progresivni)
Crop(160,0,-160,-0) # 960x720
LanczosResize(720,576) # (modw16,modh16)

# pretvori v interlaced
separatefields()
selecteven()
weave()</pre>