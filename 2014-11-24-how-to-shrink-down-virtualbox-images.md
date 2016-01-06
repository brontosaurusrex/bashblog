<http://dantwining.co.uk/2011/07/18/how-to-shrink-a-dynamically-expanding-guest-virtualbox-image/>

a. get rid of snapshots?  
(perhaps clone first)

b.

<pre>mount -n -o remount,ro -t /dev/sda1/
zerofree -v /dev/sda1</pre>

seems to do something with wheezy/ext4

(This got me down from 4.17 to 3 gigs, no snapshots preserved)