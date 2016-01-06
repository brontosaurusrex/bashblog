Copy files that are in files.txt in flat fashion to current dir;

<pre>rsync -avb --no-dirs --no-relative --files-from="files.txt" / ./</pre>