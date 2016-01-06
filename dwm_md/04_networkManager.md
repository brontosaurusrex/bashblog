## Network manager
<https://wiki.archlinux.org/index.php/NetworkManager#Other_desktops_and_window_managers>

a script like this (nmgui) can be used to show some tray and nm-applet from cli temporarily

    #!/bin/sh
    nm-applet    > /dev/null 2>/dev/null &
    trayer --widthtype pixel --width 100 --height 14 --transparent true --alpha 255 --align right > /dev/null 2>/dev/null
    # stalonetray > /dev/null 2>/dev/null
    killall nm-applet

to get straight to settings

    nm-connection-editor
    
also
    
    nm-tool # will show stats
