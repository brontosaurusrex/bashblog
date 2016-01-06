---
title: windows power shell
author: bronto saurus
layout: post
permalink: /2007/01/windows-power-shell/
categories:
  - general
---
**guides:**  
<a href="http://www.microsoft.com/technet/scriptcenter/topics/msh/cmdlets/index.mspx" target="_blank" >http://www.microsoft.com/technet/script &#8230; index.mspx</a>

**examples:**  
*dir -recurse -include *.avi | sort-object length*  
(list all avi files in folder and subfolders and sort by size, this is piping to sort-object.)

*dir | tee -file c:tee.txt*  
(dir current dir to console + write dir list to a text file)

* dir | ConvertTo-Html name,length,lastwritetime,directory -title krkej | Set-Content c:set.htm*  
(dir list to html)

<a href="http://www.microsoft.com/technet/scriptcenter/topics/msh/cmdlets/add-history.mspx" target="_blank" >http://www.microsoft.com/technet/script &#8230; story.mspx</a>  
(export, import cli history as xml)

**external urls:**  
<a href="http://en.wikipedia.org/wiki/Windows_PowerShell" target="_blank" >http://en.wikipedia.org/wiki/Windows_PowerShell</a>  
(wikipedia, interesting rss example&#8230;)