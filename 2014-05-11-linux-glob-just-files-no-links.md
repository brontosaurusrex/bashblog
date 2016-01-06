<pre>find . -maxdepth 1 -type f -print0 | xargs -0r yourCommand</pre>

or more precisely;

<pre>find . -type f -name "*.svg" -print0 | xargs -0r svgToBW</pre>