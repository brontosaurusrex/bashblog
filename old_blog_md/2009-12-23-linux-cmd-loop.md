---
title: linux cmd loop
author: bronto saurus
layout: post
permalink: /2009/12/linux-cmd-loop/
categories:
  - Uncategorized
---
example for running a shell script to make thumbs for all avis in current dir;

`for i in $(ls *avi); do makethumbwd $i; done`

(this will probably fail if filenames contain spaces&#8230;)

edit: nice&simple gui for renaming multiple files is thunar, which should be in repos and i belive it is also a default xfce file manager?

<http://thunar.xfce.org/pwiki/documentation/bulk_renamer>

[<img src="http://brontosaurusrex.69.mu/wp-content/uploads/2009/12/thunar-300x183.png" alt="" title="thunar" width="300" height="183" class="alignnone size-medium wp-image-412" />][1]

 [1]: http://brontosaurusrex.69.mu/wp-content/uploads/2009/12/thunar.png