---
title: 'encryption 2, how to change http to https&#8230;'
author: bronto saurus
layout: post
permalink: /2007/01/encryption-2-how-to-change-http-to-https/
categories:
  - web, guide
---
&#8230; using web server that does not support natively the ssl protocol?

example:  
- using web server, free version of abyss (http://www.aprelium.com/)  
- stunnel <a href="http://www.stunnel.org/" target="_blank" >http://www.stunnel.org/</a>  
*Stunnel is a program that allows you to encrypt arbitrary TCP connections inside SSL (Secure Sockets Layer)*  
So install the stunnel and configure the text file, for testing purposes the cert. found in the distro will kinda work (browsers will complain that you are bad guy thought)  
- open the ports on router (forwarding), not sure which, but 12-500 range seems to work, edit: 443 seems to be correct.  
- the pem certificate which is used by stunnel can be generated on any nix machine with openssl installed or by using online form found here:  
<a href="http://www.stunnel.org/pem/" target="_blank" >http://www.stunnel.org/pem/</a>  
- this is what opera browser will say at this point  
<img src="/images/opera_kravca_and_ssl.png" width="430" height="409" border="0" alt="" />

- the certificate part of the stunnel pem file will now be published to verysign trial certification,   
<a href="http://www.verisign.com/ssl/buy-ssl-certificates/free-ssl-certificate-trial/index.html" target="_blank" >http://www.verisign.com/ssl/buy-ssl-cer &#8230; index.html</a>  
and opera will now say  
<img src="/images/opera_kravca_and_ssl_trial_.png" width="430" height="409" border="0" alt="" />  
so who is fancy?  
and firefox snapshot of the cow:  
<img src="/images/kravca_secured.png" width="426" height="375" border="0" alt="" />

and here you can donate for this nice blog:  


&#8230; to be continued