<pre>cd /to/folder/
find . -type f -exec du -h --time --exclude='.Apple*' {} + > index.txt</pre>

then you would push that index or more of them to some web server and do a php search thingy with answer2 from here;

<http://stackoverflow.com/questions/3686177/php-to-search-within-txt-file-and-echo-the-whole-line>

edit:  
And this seems to work on osx maverick (find with white and black list and stat to get me date, file size in bytes, filename)

<pre>find . \( -name "*.mov" -o -name "*.avi" -o -name "*.jpg" -o -name "*.mp3" \) ! -path "*Adobe*" ! -path "*.pek" ! -path "*.cfa" -exec stat -f "%Sm,%z,%N" -t "%d.%m.%Y %H:%M:%S" {} + 2>/dev/null 1>index.txt</pre>

(note: version of du on osx is severely retarded as it seems)

example output  
`<br />
16.03.2007 10:32:08,17788,./raid0/xpshared2/t/utility/!!!executor/skins/medium_silver_short_listbg.jpg<br />
02.05.2007 13:14:30,9096,./raid0/xpshared2/t/utility/!!!executor/skins/medium_simpler_big_listbg.jpg<br />
15.03.2007 15:29:22,10046,./raid0/xpshared2/t/utility/!!!executor/skins/medium_simpler_listbg.jpg<br />
15.01.2009 15:52:13,467712,./raid0/xpshared2/t/utility/AudacityBeta/04_napovednik_ver1_auda2.mp3<br />
`