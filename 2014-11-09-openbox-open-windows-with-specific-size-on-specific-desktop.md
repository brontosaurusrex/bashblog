<http://crunchbang.org/forums/viewtopic.php?id=37741>

<pre>#!/bin/bash

# thuntest2
# I need 'xdotool' &lt; in repos
# open 3 thunar windows to specific positions at desktop 1 (they start with 0!)
 
now=$(xdotool get_desktop)
xdotool set_desktop 1 # &lt; change me to a desktop you want thunar windows to open

# adjust sleep as you wish
thunar ~/downloads/ &#038;&#038; sleep 3 &#038;&#038; xdotool getactivewindow windowsize 300 300 windowmove 0 30 
thunar ~/videos/ &#038;&#038; xdotool getactivewindow windowsize 300 300 windowmove 300 30
thunar ~/images/ &#038;&#038; xdotool getactivewindow windowsize 300 300 windowmove 600 30

xdotool set_desktop "$now" # return me to original desktop</pre>