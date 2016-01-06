---
title: Linux, convert docx to pdf
author: bronto saurus
layout: post
permalink: /2014/01/linux-convert-docx-to-pdf/
categories:
  - Uncategorized
---
<pre>libreoffice --headless -convert-to pdf file.docx -outdir ./</pre>

or (worse);

<pre>abiword --to=PDF -o testAbi.pdf file.docx</pre>