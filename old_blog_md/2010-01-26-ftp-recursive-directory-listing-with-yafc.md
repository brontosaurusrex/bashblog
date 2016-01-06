---
title: ftp recursive directory listing with yafc
author: bronto saurus
layout: post
permalink: /2010/01/ftp-recursive-directory-listing-with-yafc/
categories:
  - Uncategorized
---
1.  
`sudo apt-get install yafc`  
2. connect to the ftp server  
`yafc proto://user:pass@server.com`  
3.  
`ls -R > filelist.txt`  
(the filelist.txt will be writen localy)