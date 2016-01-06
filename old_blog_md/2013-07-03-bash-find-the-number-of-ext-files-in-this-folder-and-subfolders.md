---
title: 'bash, find the number of *.ext files in this folder and subfolders'
author: bronto saurus
layout: post
permalink: /2013/07/bash-find-the-number-of-ext-files-in-this-folder-and-subfolders/
categories:
  - Uncategorized
---
`find . -iname "*.ext" -printf . | wc -c`