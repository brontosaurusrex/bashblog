# DWM on fresh Debian Wheezy (2014 notes) 
with some #! and mint17 related comments

## install

install wheezy... (no desktop)

    su
    apt-get update
	apt-get install git build-essential
	su <username>
	mkdir source
	cd source
	git clone git://suckless.org/dwm && git clone git://suckless.org/dmenu
	su
	apt-get build-dep dwm
	cd dmenu
	make clean install
	cd ../dwm
	make clean install

	apt-get install xserver-xorg xorg vim
	apt-get install chromium elinks             # optional

	su <username>
	cd
	vi .xinitrc

(paste: "exec dwm" without quotes)

	startx

(dwm should start)

### enable sudo (not relatted to dwm, but something I want to do anyway)

	su
	apt-get install sudo
	adduser <username> sudo
	su <username> 
    
(logout, login or reboot ...)
