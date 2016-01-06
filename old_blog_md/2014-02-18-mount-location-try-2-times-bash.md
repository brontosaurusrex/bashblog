---
title: mount location, try 2 times, bash
author: bronto saurus
layout: post
permalink: /2014/02/mount-location-try-2-times-bash/
categories:
  - Uncategorized
---
<pre>#!/bin/bash

# Try exactly 2 times to mount a location

function doit {
	mount_smbfs "smb://user:pass@server/folder" "/Volumes/local/folder/"
	}  

doit

# check errorlevel and if not eq to 0 try to mount again
if [ $? -eq 0 ]
then
	# good
  	echo $?
  	echo "first time!"
 else
	# bad
	
   	doit # again
   	
   	echo $?
   	echo "second time?"
        # this could be improved to generate final report 
        # done / failed type.

 fi

sleep 3

</pre>