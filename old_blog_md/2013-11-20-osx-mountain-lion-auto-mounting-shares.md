---
title: 'OSX Mountain Lion > auto mounting shares'
author: bronto saurus
layout: post
permalink: /2013/11/osx-mountain-lion-auto-mounting-shares/
categories:
  - Uncategorized
---
It appears that only normal way is to write custom shell script(s) for mounts and then drop them to your user startup. A script may look like:

<pre>mount_afp "afp://user:pass@host/folder" /Volumes/Raid/NETATALK/folder
or 
mount_smbfs "smb:// .... ect"
</pre>

note: Storing passwords in text files is a security risk.

[<img src="http://brontosaurusrex.mooo.com/wp-content/uploads/2013/11/MountainLionAutoMountShares-300x259.png" alt="MountainLionAutoMountShares" width="300" height="259" size-medium wp-image-2815" />][1]

edit: on server

add 

<pre># By default all users have access to their home directories.
~/			"kresnica"</pre>

to /etc/netatalk/AppleVolumes.default

add/change stuff in /etc/netatalk/afpd.conf like

<pre>- -tcp -noddp -uamlist uams_dhx.so,uams_dhx2_passwd.so -nosavepassword -setuplog "default log_info /var/log/afpd.log</pre>

 [1]: http://brontosaurusrex.mooo.com/wp-content/uploads/2013/11/MountainLionAutoMountShares.png