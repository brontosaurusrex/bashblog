---
title: win sysinfo bat
author: bronto saurus
layout: post
permalink: /2011/11/win-sysinfo-bat/
categories:
  - Uncategorized
---
`@ECHO OFF<br />
echo .....................................................................start<br />
wmic csproduct get name,identifyingnumber,uuid<br />
wmic COMPUTERSYSTEM get TotalPhysicalMemory,caption<br />
wmic bios get name,serialnumber,version<br />
wmic cpu get name,CurrentClockSpeed,MaxClockSpeed<br />
echo .....................................................................drives<br />
wmic logicaldisk WHERE drivetype=3 GET name,freespace,SystemName,FileSystem,Size,VolumeSerialNumber<br />
wmic diskdrive get name,size,model<br />
echo .....................................................................nic<br />
wmic nic get macaddress,description<br />
echo .....................................................................systeminfo<br />
systeminfo<br />
echo .....................................................................end`