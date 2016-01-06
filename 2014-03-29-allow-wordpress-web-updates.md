Basically all wp files must be owned by the process running the wp, this did the trick for me;

<pre>sudo chown -R www-user:www-user ./</pre>

Then go to your wp-admin and run the updates &#8230;