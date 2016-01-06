---
title: Mountain lion os x, add refresh button to finder
author: bronto saurus
layout: post
permalink: /2014/04/mountain-lion-os-x-add-refresh-button-to-finder/
categories:
  - Uncategorized
---
in automator make a new app, add &#8220;run applescript&#8221; thingy with;

<pre>on run {input, parameters}
	
	tell application "Finder" to tell front window to update every item
	
	return input
end run
</pre>

save as app, drag and drop to finder buttons.

[<img src="http://brontosaurusrex.mooo.com/wp-content/uploads/2014/04/automator-300x264.png" alt="automator" width="300" height="264" class="alignleft size-medium wp-image-3064" />][1]

[<img src="http://brontosaurusrex.mooo.com/wp-content/uploads/2014/04/here-300x216.png" alt="here" width="300" height="216" class="alignleft size-medium wp-image-3065" />][2]

 [1]: http://brontosaurusrex.mooo.com/wp-content/uploads/2014/04/automator.png
 [2]: http://brontosaurusrex.mooo.com/wp-content/uploads/2014/04/here.png