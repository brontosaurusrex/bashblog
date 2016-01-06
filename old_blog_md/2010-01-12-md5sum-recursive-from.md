---
title: md5sum recursive from ./
author: bronto saurus
layout: post
permalink: /2010/01/md5sum-recursive-from/
categories:
  - Uncategorized
---
make md5 file  
`find . -type f -exec md5sum {} ; >> checkall.md5`

check with md5 file  
`md5sum -c checkall.md5`

how to compile md5sum under osx  
<http://blog.raamdev.com/2008/10/11/howto-install-md5sum-sha1sum-on-mac-os-x>

<pre lang="bash">$ ./configure
$ make
$ sudo make install
cp md5sum sha1sum ripemd160sum /usr/local/bin
chown bin:bin /usr/local/bin/md5sum /usr/local/bin/sha1sum 
/usr/local/bin/ripemd160sum
chown: bin: Invalid argument
make: *** [install] Error 1</pre>

sources: <http://www.microbrew.org/tools/md5sha1sum/>