mount

<pre>apt-get install jmtpfs
cd
mkdir here
jmtpfs here</pre>

and it should mount (connected with usb cable)

unmount

<pre>fusermount -u</pre>

edit: behaviour is buggy and slow.

a switch script could look like this (directory ~/here is supposed to exist)

<pre>#!/bin/bash

if mount -l | grep here; then 
    echo "is mounted here, unmounting now";
    fusermount -u ~/here
    
    else
    echo "not mounted here, mounting now";
    jmtpfs ~/here
    open ~/here


fi
</pre>

and an unrelated scrot of mint17 in action  
[<img src="http://shrani.si/t/3N/Fz/3yep5fFy/htc.jpg" style="border: 0px;" alt="Shrani.si" />][1]

 [1]: http://shrani.si/f/3N/Fz/3yep5fFy/htc.png