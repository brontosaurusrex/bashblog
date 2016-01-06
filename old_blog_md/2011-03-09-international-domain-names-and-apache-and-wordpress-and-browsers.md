---
title: international domain names and apache and wordpress and browsers
author: bronto saurus
layout: post
permalink: /2011/03/international-domain-names-and-apache-and-wordpress-and-browsers/
categories:
  - Uncategorized
---
***apache:*** host name should be defined using punnycode, not the real chars, for example (domain name would be štala.si):

in /etc/apache2/sites-enabled make a site named: www.xn--tala-f6a.si

`<br />
ServerName www.xn--tala-f6a.si<br />
ServerAlias www.xn--tala-f6a.si<br />
ServerAdmin email@mymail.com<br />
DocumentRoot /home/user/public_html/stala/<br />
`

and

file xn--tala-f6a.si, with similar content.

***browsers:*** (it appears that on windows: ie7 and chrome are behaving nicely)  
Firefox: about:config and add this to the whitelist:  
network.IDN.whitelist.si;true  
(this is of course very useless for your visitors, they will have to stare at weird looking punnycode)

***wordpress:***  
use punnycode and not the real chars, when defining the site.