
# Rtorrent + Rutorrent Auto Install Script by me, a modified version of Bercik's scipt what is a modified version of Kerwood's script
### Modern script for automatic rtorrent, rutorrent installation under Linux.
	Makes your system seedbox ready in minutes!

![Logo](https://i.imgur.com/KtvJriL.jpg)

## News

**Current version** v2.5 released 2024/12/18

	* always use of the latest ruTorrent
	* no need to care about the distro version
	* remove unnecessary stuff
	* add support for arm* systems (scgi)
	* correcting external ipv4
	* deactivate not supportet plugins
	* redirect http to https
	* correct terminal colors
	* add autodl-irssi plugin (Rt-Install-minimal-new.bash)
	* update .rtorrent.rc to the new commands
	* fix changelog and todo view
	* put functions together for more order
	* make pre-installation packages fully silent
	* and a little bit there and there
	* now choose between apache2, nginx and lighttpd as webserver (Rt-Install-minimal-apache2_ngnix_lighttpd.bash)
	* create htaccess passwords now with openssl
	* remove ToDo-List from the Menu
	* move from SCGIMount to rpc.socket
	* hardening the webserver basend on https://raymii.org/s/tutorials/Strong_SSL_Security_On_*.html
	* reintegrade To-Do List
	* putting rtorrent and rutorrent user determination inside the menu and prevent installation to start without
	* add function to update ruTorrent
	* reactivate plugins screenshots, spectrogram
	* some corrections
	* adopt the actual ruTorrent branches (v4 & v5) since autodl is brocken in v5

## Features ##

* This script performs automatic installation of rTorrent (BitTorrent client) and ruTorrent (web based GUI).
* It detects your OS and uses most recent version of rT available in repository of your Linux distribution.
* Gives menu-driven guidance when creating username.
* This script is minimal inversiv to files and operating system
* Free choose between apache2, ngnix or lighttpd as webserver

## Supported operating systems ##

* **Debian**
* **Raspbian**
* **Ubuntu**
* **Mint**
* **LMDE**

## What the scripts does ##
In the installation process you have to choose a system user to run rtorrent. The script add a service that
makes rtorrent start, at a possible reboot, in the given username's tmux session. Use "systemctl rtorrent start"
and "systemctl rtorrent stop" to start and stop rtorrent respectively.

Run the script with sudo or as root
	
	git clone https://github.com/MarkusLange/rt-auto-install.git
	cd rt-auto-install
	sudo ./Rt-Install-minimal-apache2_ngnix_lighttpd_prc-socket_choose_branche.bash
	
 	with autodl-irssi, rpc.socket (no SCGIMount anymore) and update function for ruTorrent and options to choose the ruTorrent branche
	wget https://raw.githubusercontent.com/MarkusLange/rt-auto-install/master/Rt-Install-minimal-apache2_ngnix_lighttpd_prc-socket_choose_branche.bash

## To-Do ##
* Add Wiki to explain what is, and why something is done (only someone is interested)
* ~~remove the SCGI code from the scrip is atm. deactivated~~
* ~~remove other commented out parts from the script to clean it update~~
* put some effort in a wider testbase rewriting was done on debian 12.5 only (with countless VMs)
* ~~may transfer naming and links to this fork so there is less confusion for users~~
* ~~also transfer changelog and To-Do~~
* working out with Bercik when he is less busy what he liked to merged
* remove/deactivate webserver default pages
