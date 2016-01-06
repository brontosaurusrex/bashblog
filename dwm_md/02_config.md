## configure: 
    vi config.h
... to your liking
mine here: <https://dl.dropboxusercontent.com/u/79532365/dwm/config.h.bronto>
and

    sudo make clean install

### patching
copy the diff to source/dwm, then
    
    patch < dwm-6.1-systray.di
fixme    
    
## status bar and startup

    sudo vi /usr/local/bin/dwm_status
and make a bash like;

    #!/bin/bash
    while true; do
        date=`date +"%x %H:%M"`
        xsetroot -name "$date" # leave some space for trayer, oh rly?
    sleep 30
    done

or more complex

    #!/bin/bash
    while true; do
      date=`date +"%a %d.%m.%y %H:%M"`
      speed=`awk '{if(l1){print int(($2-l1)/1024+.5),int(($10-l2)/1024+.5)" kB/s"} else{l1=$2; l2=$10;}}' <(grep eth0 /proc/net/dev) <(sleep 1; grep eth0 /proc/net/dev)`
      disk=`df -hl /home/b/videos | tail -n 1 | cut -c 28-32`
      info="$speed$disk $date"
    #  echo $info # disable
      xsetroot -name "$info" 
      sleep 13
    done

sudo chmod +x /usr/local/bin/dwm_status

    cd
    vi .xinitrc

paste
    
    userresources=$HOME/.Xresources
    usermodmap=$HOME/.Xmodmap
    sysresources=/etc/X11/xinit/.Xresources
    sysmodmap=/etc/X11/xinit/.Xmodmap

    if [ -f $sysresources ]; then
        /usr/bin/xrdb -merge $sysresources
    fi

    if [ -f $sysmodmap ]; then
        /usr/bin/xmodmap $sysmodmap
    fi

    if [ -f $userresources ]; then
        /usr/bin/xrdb -merge $userresources
    fi

    if [ -f $usermodmap ]; then
        /usr/bin/xmodmap $usermodmap
    fi

    # this will need dropbox.py (renamed to dropbox) 
    # somewhere on the path

    dropbox start &

    # start urxvt daemon (start urxvt with urxvtc later, in dwm config.h) 
    urxvtd -q -f -o &

    nitrogen --restore & # load wallpaper

    compton &            # optional

    dwm_status &
    exec ck-launch-session dbus-launch dwm
