## ON MINT 17 with xsessions

It is interesting that login manager approach does work as expected with mint 17 (ubuntu based), for example, making file
    
    /usr/share/xsessions/dwm.desktop

filled with

    [Desktop Entry]
    Encoding=UTF-8
    Name=Dwm
    Comment=Dynamic window manager
    Exec=dwm_start
    Icon=dwm
    Type=XSession

where dwm_start is my custom start script (copy/pasted .xinitrc to /usr/local/bin/dwm_start)

warning: mdm login manager and infinity fonts may have problems withj each other

fix:

    sudo mv /etc/profile.d/infinality-settings.sh /etc/infinality-settings.sh
    sudo chmod a+rx /etc/infinality-settings.sh

To .bashrc, add:

    # INFINALITY FONT RENDERING CONFIG
    . /etc/infinality-settings.sh

from <http://superuser.com/questions/558974/linux-mint-fails-to-start-x-automatically-after-update-but-x-still-works>


# scrots 2
<http://shrani.si/f/3I/qE/sH5QxGT/mintdwm.png>
<http://shrani.si/f/l/NI/1dhxwTyV/mint17dwm2.png>
<http://shrani.si/f/12/gq/oJmTmrc/pixelmoon.png>
<http://shrani.si/f/2A/Iq/3A9TyBGl/tabpatch.png>
<http://shrani.si/f/s/Xv/4ibqhS6s/psy.png>

end
