<pre>#!/bin/bash

# simple pasta countup clock
# needs 'figlet' from repos

# checks
command -v figlet >/dev/null 2>&#038;1 || { echo "apt-get install figlet"; exit 1; } 

date1=`date +%s`; while true; do 

     # clear
     # echo -ne "\r$(date -u --date @$((`date +%s` - $date1)) +%H:%M:%S)";
     # nice -n 19 toilet -f ascii12 $(echo -ne "\r$(date -u --date @$((`date +%s` - $date1)) +%H:%M:%S)";);
     # nice -n 19 toilet -f standard $(echo -ne "\r$(date -u --date @$((`date +%s` - $date1)) +%H:%M:%S)";);

     nice -n 19 figlet -f mono9 $(echo -ne "\r$(date -u --date @$((`date +%s` - $date1)) +%H:%M:%S)";);


sleep 1

done

</pre>