---
title: canon 7d footage avisynth examples
author: bronto saurus
layout: post
permalink: /2010/08/canon-7d-footage-avisynth-examples/
categories:
  - Uncategorized
---
<pre lang="avisynth">LoadPlugin("t:utilityavisynthffmpegsourceFFMS2.dll")
a=FFaudioSource("E:brontosaurusrexcanon7d2010_07_31MVI_0170.MOV")
v=FFVideoSource("E:brontosaurusrexcanon7d2010_07_31MVI_0170.MOV")
AudioDub(v, a)</pre>

or

<pre lang="avisynth">LoadPlugin("t:utilityavisynthffmpegsourceFFMS2.dll")
FFVideoSource("D:brontosaurusrexCITYd7MVI_5817.MOV")
assumefps(25)
resize(720,576)
killaudio()</pre>