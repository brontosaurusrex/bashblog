---
title: rsync strikes back
author: bronto saurus
layout: post
permalink: /2012/08/rsync-strikes-back/
categories:
  - Uncategorized
---
not tested, just theory so far:

<http://articles.slicehost.com/2007/10/10/rsync-exclude-files-and-folders>  
<http://examplenow.com/rsync/>

to exclude something use &#8211;exclude-from (Using the &#8211;exclude-from option solved it by preventing the shell expansion of the wildcard entries.)

example to be used for local (non-server usage, &#8211;times is important!!!):

`rsync -rvh --times --progress --exclude-from<br />
/Volumes/this/must/be/absolute/path/exclude.txt /from/here/ /to/there/`

where exclude.txt may look like:

*.pek  
Adobe Premiere Pro Preview*