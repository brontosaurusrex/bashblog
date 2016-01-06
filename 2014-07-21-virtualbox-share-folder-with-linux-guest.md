specifically: osx=host, linux mint=guest

use the virtualbox gui to define a shared folder, scrot

[<img src="http://brontosaurusrex.mooo.com/wp-content/uploads/2014/07/vbox_shared_folder.png" alt="vbox_shared_folder" width="589" height="390" class="aligncenter size-full wp-image-3312" />][1]

add **existing** user to a vbox group named **vboxsf**, if user name is **testuser**;

<pre>sudo usermod -a -G vboxsf testuser</pre>

now the shared folder should automount (reboot) in 

<pre>/media/sf_Dropbox</pre>

linkage [https://www.virtualbox.org/manual/ch04.html#sf\_mount\_auto][2]

 [1]: http://brontosaurusrex.mooo.com/wp-content/uploads/2014/07/vbox_shared_folder.png
 [2]: https://www.virtualbox.org/manual/ch04.html#sf_mount_auto