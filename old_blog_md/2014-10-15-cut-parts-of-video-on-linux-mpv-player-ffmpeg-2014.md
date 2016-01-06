---
title: cut parts of video on linux (mpv player + ffmpeg 2014)
author: bronto saurus
layout: post
permalink: /2014/10/cut-parts-of-video-on-linux-mpv-player-ffmpeg-2014/
categories:
  - Uncategorized
---
a. use mpv to locate the cut points;

<pre>mpv --osd-fractions input.mp4</pre>

To copy current video position to clipboard add

<pre>Meta+c run "/bin/sh" "-c" "/bin/echo -n ${time-pos/full} | xsel --clipboard --input"</pre>

(Debian wheezy)  
to .mpv/input.conf and then use Meta (Thats usually win-key to copy).

btw: Use , and . to move frame by frame.

b. use ffmpeg to cut the video

<pre>ffmpeg -i input.mp4 -ss 00:01:45.480 -to 00:01:46.606 (video,audio codec parameters here) part.mp4</pre>

screenshot  
[<img src="http://brontosaurusrex.mooo.com/wp-content/uploads/2014/10/mpvUndffmpeg-300x246.png" alt="mpvUndffmpeg" width="300" height="246" class="aligncenter size-medium wp-image-3475" />][1]

related:  
<http://crunchbang.org/forums/viewtopic.php?pid=399702#p399702>

 [1]: http://brontosaurusrex.mooo.com/wp-content/uploads/2014/10/mpvUndffmpeg.png