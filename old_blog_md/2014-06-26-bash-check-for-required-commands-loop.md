---
title: bash, check for required commands, loop
author: bronto saurus
layout: post
permalink: /2014/06/bash-check-for-required-commands-loop/
categories:
  - Uncategorized
---
<pre>commands="/usr/bin/ffmpegthumbnailer /usr/bin/convert thing ffmpeg"
 
for i in $commands
do
    # command -v will return >0 when the $i is not found
	command -v $i >/dev/null &#038;&#038; continue || { echo "$i command not found."; exit 1; }
done
</pre>

bash guide, pdf  
<http://folk.ntnu.no/geirha/bashguide.pdf>