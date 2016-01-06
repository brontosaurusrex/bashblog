<pre>./ffmpeg -i big_buck_bunny_720p_h264.mov -vf 'select=gt(scene\,.4),showinfo' -f null - 2>&#038;1 | sed 's/.*pts_time:\([[:digit:].]*\).*/\1/'

./ffmpeg -i big_buck_bunny_720p_h264_prores.mov -vf 'scale=300:300,select=gt(scene\,.4),showinfo' -f null - 2>&#038;1 | sed 's/.*pts_time:\([[:digit:].]*\).*/\1/'

./ffmpeg -i big_buck_bunny_720p_h264_prores.mov -sws_flags neighbor -vf 'scale=100:100,select=gt(scene\,.4),showinfo' -f null - 2>&#038;1 | sed 's/.*pts_time:\([[:digit:].]*\).*/\1/'

kako z bashem do edla:

http://stackoverflow.com/questions/5199806/bash-how-to-make-timecode-calculations

V bistvu bo treba vse pretvorit v frejme, računati v frejmih, nato pa spluvati ven v
hh.mm.ss.ff formatu &lt; (šele tule bo treba razlikovat FPS!!!)</pre>

Work in Progress, script, edls, ect  
<https://www.dropbox.com/sh/ljj2kk24pudp5un/AABIqjOO0iHVGJwcHnVl8w3wa?dl=0>