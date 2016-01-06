---
title: search drives for files with string (os x bash)
author: bronto saurus
layout: post
permalink: /2013/12/search-drives-for-bash/
categories:
  - Uncategorized
---
usage:  
metafind string  
or  
metafind &#8220;string with spaces&#8221;

in sequence;

<pre>#!/bin/bash

dirs=( "/Volumes/PROMOCIJA" "/Volumes/Disk1" "/Volumes/Disk2" "/Volumes/Disk3" "/Volumes/Disk4" "/Volumes/Disk5" "/Volumes/Disk6" "/Volumes/Disk7" "/Volumes/GRAFIKA" )

for i in "${dirs[@]}"
do

echo searching "$i"
find "$i" | grep -i -s -e "$@"

done

exit</pre>

all at once;

<pre>#!/bin/bash

trap 'kill $(jobs -p)' EXIT

dirs=( "/Volumes/PROMOCIJA" "/Volumes/Disk1" "/Volumes/Disk2" "/Volumes/Disk3" "/Volumes/Disk4" "/Volumes/Disk5" "/Volumes/Disk6" "/Volumes/Disk7" "/Volumes/GRAFIKA" )

for i in "${dirs[@]}"
do

echo searching "$i"
find "$i" | grep -i -s -e "$@" &#038;




done

wait

exit</pre>