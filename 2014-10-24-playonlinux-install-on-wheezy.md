<http://www.playonlinux.com/en/download.html>  
the addkey command should use sudo for the apt-key part;

<pre>wget -q "http://deb.playonlinux.com/public.gpg" -O- | sudo apt-key add -</pre>