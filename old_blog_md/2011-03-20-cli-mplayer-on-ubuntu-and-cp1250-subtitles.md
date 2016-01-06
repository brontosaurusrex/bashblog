---
title: cli mplayer on ubuntu and cp1250 subtitles
author: bronto saurus
layout: post
permalink: /2011/03/cli-mplayer-on-ubuntu-and-cp1250-subtitles/
categories:
  - Uncategorized
---
the solution seems to be a two step process:

1. convert cp1250 to unicode, maybe with a script like (compatible with nautilus script folder):

*iconv\_cp1250\_to_utf8*

<pre lang="bash">#!/bin/bash

while [ $# -gt 0 ]; do
	
file=$1
filename=${file%.*}
extension=${file##*.}

iconv $1 -o $filename_utf8.srt --from-code=cp1250 --to-code=utf8

shift
done

# primer
#  iconv subtitle1250.srt -o unicode.srt --from-code=cp1250 --to-code=utf8</pre>

2. make sure that your* ~/.mplayer/config* has:

<pre lang="bash"># Set font encoding.
subfont-encoding=unicode

# Set subtitle file encoding.
unicode=yes
utf8=yes</pre>