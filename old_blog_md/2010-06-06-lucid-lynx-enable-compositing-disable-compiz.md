---
title: lucid lynx enable compositing (disable compiz)
author: bronto saurus
layout: post
permalink: /2010/06/lucid-lynx-enable-compositing-disable-compiz/
categories:
  - Uncategorized
---
There seems to be a compiz related bug where there is no chance to change the cursor size, enabling compositing and disabling compiz seems to be the current fasion around this bug, like so, compositing on:

`gconftool-2 -s --type bool /apps/metacity/general/compositing_manager true`  
and off  
`gconftool-2 -s --type bool /apps/metacity/general/compositing_manager false`  
[<img src="http://brontosaurusrex.69.mu/wp-content/uploads/2010/06/fatso.png" alt="" title="fatso" width="200" height="245" class="alignnone size-full wp-image-904" />][1]

more  
[http://ubuntu-tutorials.com/2009&#8230;][2]

 [1]: http://brontosaurusrex.69.mu/wp-content/uploads/2010/06/fatso.png
 [2]: http://ubuntu-tutorials.com/2009/02/25/update-enable-compositing-the-easier-way/