---
title: fail2ban apache post-flood filter
author: bronto saurus
layout: post
permalink: /2014/12/fail2ban-apache-post-flood-filter/
categories:
  - Uncategorized
---
<http://klcollins.org/2013/09/fail2ban-love/>

I did is slightly differently, add to jail.local;

<pre>[apache-postflood]
enabled = true
port = http,https
filter = apache-postflood
action = iptables-multiport[name=apache-postflood, port="http,https", protocol=tcp]
logpath = /var/log/apache2/access.log
maxretry = 20
bantime = 5000
</pre>

add to ./filter.d/apache-postflood.conf

<pre># Fail2Ban configuration file
#
#
# $Revision: 1 $
#
 
[Definition]
# Option: failregex
# Notes.: Regexp to catch known spambots and software alike. Please verify
# that it is your intent to block IPs which were driven by
# abovementioned bots.
# Values: TEXT
#
failregex = ^&lt;HOST> -.*."POST"*
# Option: ignoreregex
# Notes.: regex to ignore. If this regex matches, the line is ignored.
# Values: TEXT
#
ignoreregex =</pre>

restart fail2ban.

p.s. to test the filter;

<pre>fail2ban-regex /var/log/apache2/access.log /etc/fail2ban/filter.d/apache-postflood.conf > ~/test.txt &#038;&#038; geany ~/test.txt</pre>