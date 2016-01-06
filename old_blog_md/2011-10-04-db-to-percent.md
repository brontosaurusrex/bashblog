---
title: dB to percent
author: bronto saurus
layout: post
permalink: /2011/10/db-to-percent/
categories:
  - Uncategorized
---
[http://www.ehow.co.uk/how\_8643686\_convert-db-loss-percent.html][1]

*For example, a loss of 3 db of sound is equivalent to a decrease of  
10 ^ (-3 / 20) * 100 = 70.8%.  
-3 is used since this is a loss, so the variation is negative.*

bc, this seems to work:  
`echo "100*e((-3/20)*l(10))"|bc -l`

 [1]: http://www.ehow.co.uk/how_8643686_convert-db-loss-percent.html