---
title: win cmd and unicode
author: bronto saurus
layout: post
permalink: /2008/06/win-cmd-and-unicode/
categories:
  - general
---
<a href="http://www.dpawson.co.uk/xsl/sect2/Unicode.html" target="_blank" >http://www.dpawson.co.uk/xsl/sect2/Unicode.html</a>

*Trigger the unicode support for all pipe etc (default is ansi) with the command:</p> 

cmd /u

Set the font of the console to one that has glyphs in the unicode range:  
- go to console system menu (Alt-Space)  
- select Properties > Font  
- select &#8220;Lucida Sans&#8221; (MS will automatically select &#8220;Lucida Sans Unicode&#8221; when it is needed and when it is available on your system)

Change the codepage of the console screen to use Unicode (default is IBM 437) with the command:

chcp 65001

Call your commands \*without\* using a batch file (won't work anymore&#8230;). You can put your command in an environment variable for nconvenience.</i>