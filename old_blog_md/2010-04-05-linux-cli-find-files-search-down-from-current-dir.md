---
title: linux cli, find files for dummies (search down from current dir)
author: bronto saurus
layout: post
permalink: /2010/04/linux-cli-find-files-search-down-from-current-dir/
categories:
  - Uncategorized
---
&#8216;string&#8217; is the filename we are searching for

one way:  
`find ./ -name *string*`  
(will find files with string in them)

the other way:  
`alias ds='find . | grep -s -e '` then  
`ds string`  
(will find files and folders with string in them)

the other way and a half:  
`alias easyfind='find . | grep -i -s -e '`  
`easyfind StRinG`  
(will find files and folders with string in them, ignoring case)

p.s. to make alias permanent, dump it to your .bashrc,  
`gedit /home/user/.bashrc &#038;`

edit: there is also a wonderfull  
`locate`  
command which will do similar thing&#8230;, oh well, something new every day ;)

or a bash script that you could dump to ~/bin

<pre>find . 2>&#038;1 | grep -v 'Permission denied' | grep -i -s -e "$@"</pre>

Same as the alias, but will also hide permission denied errors.