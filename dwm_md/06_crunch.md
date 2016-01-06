## ON CRUNCHBANG

After playing around with slim for a bit

    sudo apt-get remove slim

Make two .xinitrc files

.xinitrc_openbox

    exec /usr/bin/openbox-session

and## ON CRUNCHBANG

After playing around with slim for a bit

    sudo apt-get remove slim

Make two .xinitrc files

.xinitrc_openbox

    exec /usr/bin/openbox-session

and
.xinitrc_dwm

    see examples above
    
after console login do

    cp .xinitrc_dwm or .xinitrc_openbox to .xinitrc
    startx

## AUTOMOUNT IN THUNAR

external devices (at least ntfs) are not mounting in thunar with error: permission denied < fixed with latest .xinitrc

workaround:

    cd
    mkdir ntfs
    fdisk -l | grep ntfs
    sudo mount -t ntfs /dev/sdXY ~/ntfs

## NOT WORKING or WEIRD

- shift + mod + q seems to lead to violent X exit, crashing the apps
- dwm should be probably started in a while loop, test

## XRESOURCES example

.Xresources (urxvt)

    URxvt*geometry:         112x22  
    URxvt*font:             -*-terminus-medium-*-*-*-*-140-*-*-*-*-iso8859-1
    URxvt*boldFont:     
    URxvt*urlLauncher:      firefox  
    URxvt*scrollBar:        false
    URxvt*scrollBar_right:  true
    URxvt*scrollColor:      #000000

    != dwm-colors = ! 
     
    *background: #222222
    *foreground: #eeeeee
    *cursorColor: #B15C00 
     
    !! black dark/light
    *color0: #222222
    *color8: #444444

    !! red dark/light
    *color1: #B10000
    *color9: #CC0000

    !! green dark/light
    *color2: #6CB100
    *color10: #7CCC00

    !! yellow dark/light
    *color3: #B15C00
    *color11: #CC6A00

    !! blue dark/light
    *color4: #005577
    *color12: #0075A3

    !! magenta dark/light
    *color5: #5600B1
    *color13: #6300CC
    *color13: #CC69B9

    !! cyan dark/light
    *color6: #007177
    *color14: #009199

    !! white dark/light
    *color7: #bbbbbb
    *color15: #eeeeee  


note: enable bitmap fonts

colors from <https://bbs.archlinux.org/viewtopic.php?id=51818&p=8>
.xinitrc_dwm

    see examples above
    
after console login do

    cp .xinitrc_dwm or .xinitrc_openbox to .xinitrc
    startx
## ON CRUNCHBANG

After playing around with slim for a bit

    sudo apt-get remove slim

Make two .xinitrc files

.xinitrc_openbox

    exec /usr/bin/openbox-session

and
.xinitrc_dwm

    see examples above
    
after console login do

    cp .xinitrc_dwm or .xinitrc_openbox to .xinitrc
    startx

## AUTOMOUNT IN THUNAR

external devices (at least ntfs) are not mounting in thunar with error: permission denied < fixed with latest .xinitrc

workaround:

    cd
    mkdir ntfs
    fdisk -l | grep ntfs
    sudo mount -t ntfs /dev/sdXY ~/ntfs

## NOT WORKING or WEIRD

- shift + mod + q seems to lead to violent X exit, crashing the apps
- dwm should be probably started in a while loop, test

## XRESOURCES example

.Xresources (urxvt)

    URxvt*geometry:         112x22  
    URxvt*font:             -*-terminus-medium-*-*-*-*-140-*-*-*-*-iso8859-1
    URxvt*boldFont:     
    URxvt*urlLauncher:      firefox  
    URxvt*scrollBar:        false
    URxvt*scrollBar_right:  true
    URxvt*scrollColor:      #000000

    != dwm-colors = ! 
     
    *background: #222222
    *foreground: #eeeeee
    *cursorColor: #B15C00 
     
    !! black dark/light
    *color0: #222222
    *color8: #444444

    !! red dark/light
    *color1: #B10000
    *color9: #CC0000

    !! green dark/light
    *color2: #6CB100
    *color10: #7CCC00

    !! yellow dark/light
    *color3: #B15C00
    *color11: #CC6A00

    !! blue dark/light
    *color4: #005577
    *color12: #0075A3

    !! magenta dark/light
    *color5: #5600B1
    *color13: #6300CC
    *color13: #CC69B9

    !! cyan dark/light
    *color6: #007177
    *color14: #009199

    !! white dark/light
    *color7: #bbbbbb
    *color15: #eeeeee  


note: enable bitmap fonts

colors from <https://bbs.archlinux.org/viewtopic.php?id=51818&p=8>
## AUTOMOUNT IN THUNAR

external devices (at least ntfs) are not mounting in thunar with error: permission denied < fixed with latest .xinitrc

workaround:

    cd
    mkdir ntfs
    fdisk -l | grep ntfs
    sudo mount -t ntfs /dev/sdXY ~/ntfs

## NOT WORKING or WEIRD

- shift + mod + q seems to lead to violent X exit, crashing the apps
- dwm should be probably started in a while loop, test

## XRESOURCES example

.Xresources (urxvt)

    URxvt*geometry:         112x22  
    URxvt*font:             -*-terminus-medium-*-*-*-*-140-*-*-*-*-iso8859-1
    URxvt*boldFont:     
    URxvt*urlLauncher:      firefox  
    URxvt*scrollBar:        false
    URxvt*scrollBar_right:  true
    URxvt*scrollColor:      #000000

    != dwm-colors = ! 
     
    *background: #222222
    *foreground: #eeeeee
    *cursorColor: #B15C00 
     
    !! black dark/light
    *color0: #222222
    *color8: #444444

    !! red dark/light
    *color1: #B10000
    *color9: #CC0000

    !! green dark/light
    *color2: #6CB100
    *color10: #7CCC00

    !! yellow dark/light
    *color3: #B15C00
    *color11: #CC6A00

    !! blue dark/light
    *color4: #005577
    *color12: #0075A3

    !! magenta dark/light
    *color5: #5600B1
    *color13: #6300CC
    *color13: #CC69B9

    !! cyan dark/light
    *color6: #007177
    *color14: #009199

    !! white dark/light
    *color7: #bbbbbb
    *color15: #eeeeee  


note: enable bitmap fonts

colors from <https://bbs.archlinux.org/viewtopic.php?id=51818&p=8>
