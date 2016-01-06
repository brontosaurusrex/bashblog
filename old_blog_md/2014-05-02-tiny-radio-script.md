---
title: tiny radio script
author: bronto saurus
layout: post
permalink: /2014/05/tiny-radio-script/
categories:
  - Uncategorized
---
<http://linuxbbq.org/bbs/viewtopic.php?f=4&t=1168&p=21911&hilit=pidsley+radio#p21911>

(add -b 2000 to mpg123 line to get some buffering)

edit: and a mpv edition (mpv supports more audio formats);

<pre>#!/bin/bash

STREAM_FILE=~/bin/radiolist

[[ ! -f "$STREAM_FILE" ]] &#038;&#038; echo "$STREAM_FILE does not exist" &#038;&#038; exit 1

array=( $(cat "$STREAM_FILE") )

select opt in "${array[@]}"; do
    [[ $1 =~ ^-r ]] &#038;&#038; streamripper "$opt" &#038;
    # mpg123 -b 2000 -@ "$opt"
    mpv --load-unsafe-playlists "$opt" --cache 1000 --msglevel=cplayer=no:ffmpeg/audio=no:ffmpeg/demuxer=no:ffmpeg/video=no:ad=no --no-video
    break
done
</pre>