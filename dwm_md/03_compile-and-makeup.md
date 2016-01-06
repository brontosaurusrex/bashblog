## compile/install compton (from git)

    apt-get install libx11-dev libxcomposite-dev libxdamage
    apt-get install libxext-dev libxrender-dev libxrandr-dev libxinerama-dev pkg-config 
    apt-get install libpcre3-dev libconfig-dev libdrm-dev libgl-gst asciidoc
(this will pull in a lot of stuff)

git clone the compton git

    make
    make docs
    sudo make install
    
## gtk makeup
    apt-get install lxapperance feh scrot gtk2-engines-pixbuf gtk2-engines-murrine

## infinality 
(with some googling I found premade debs) 
<https://wiki.debian.org/Fonts>
<http://forums.debian.net/viewtopic.php?f=16&t=88545>

to configure 

    sudo bash /etc/fonts/infinality/infctl.sh setstyle

## MPV. mpv player
get the mpv-build git , cd to source/mpv-build and
next three lines should install all dependencies for build

    sudo apt-get install devscripts equivs
    rm -f mpv-build-deps_*_*.deb
    mk-build-deps -s sudo -i

> from <https://github.com/mpv-player/mpv-build>

and the usual

    ./rebuild -j2

## SUBLIME to path (or at least for current user)

    sudo vi /usr/bin/sublime

and paste

    export sublime_home="/home/b/apps/sublime"
    $sublime_home/sublime_text "$*"

then

    sudo chmod 775 /usr/bin/sublime 

### sublime user settings, optional

    {
        "color_scheme": "Packages/Color Scheme - Default/Monokai.tmTheme",
    	"font_face": "terminus",
    	"font_size": 12,
    	"word_wrap": true
    }
