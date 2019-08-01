
# Rtorrent + Rutorrent Auto Install Script by Bercik
### Modern script for automatic rtorrent, rutorrent installation under Linux.
	Makes your system seedbox ready in minutes!



## News

**Current version** v0.5 released 2019/08/01
We CLI parameters:
Added "demo" mode. It hides your public IP at the end.            (-d --demo)
Added "fast" mode. It drops all slowdowns, for people in a hurry. (-f --fast)
Added "help" parameter.                                           (-h --help)
Menu displays only 15 recent lines of Changelog and TODO.

For details, always go to Changelog.

## Features ##

* This script performs automatic installation of rTorrent (BitTorrent client) and ruTorrent(web based GUI).
* It detects your OS and uses most recent version of rT available in repository of your Linux distribution.
* Uses SINGLE file for all supported operating systems.
* Gives menu-driven guidance when creating username.
* It's actively developed and I'm not planning to drop it like others did :P

## Supported operating systems ##
* **Debian 10    Buster**
* **Raspbian 10  Buster**
* **Ubuntu 19.04 Disco Dingo**
* **Ubuntu 18.10 Cosmic Cuttlefish**
* **Ubuntu 18.04 Bionic Beaver**
* **Mint   19.01 Tessa**
* **Mint   19    Tara**

More to come, see TODO.

## What the scripts does ##
In the installation process you have to choose a system user to run rtorrent.
Also you will get the opportunity of installing a total of 46 plugins. See list further down.
The script add a init script that makes rtorrent start, at a possible reboot, in the
given username's screen/tmux session. Use "service rtorrent-init start" and
"service rtorrent-init stop" to start and stop rtorrent respectively.


Installation
------------

**Installation video**

[![rt-auto-install script youtube](https://img.youtube.com/vi/uBxfSg0blPM/0.jpg)](https://www.youtube.com/watch?v=uBxfSg0blPM)

Old video for v0.1 here -> https://www.youtube.com/watch?v=B3n2fE1Eo9Y


Run the script with sudo or as root
	
	git clone https://github.com/Bercik1337/rt-auto-install.git
	cd rt-auto-install
	sudo ./Rt-Install-minimal

FAQ
------------
### But _WHY_ if we have Docker version?
I took over abandoned installation script because author didn't want to develop it anymore. Excuse was that everything moved to Docker.

In my personal opinion that's a **bad move**, and no one else fixed script - so I did. Docker itself is not a bad idea, but I would like to see it in dynamic, scalable environments where it grows and shrinks depending on workload.

That's certainly NOT the case here. rtorrent is ran usually 24/7, does not work in cluster solutions or anything close to that. So sticking it into Docker is 1. waste of resources (CPU, disk) 2. Security risk (everything you'd normally have PLUS Docker problems).
I might be the only person using this script - so be it. No containers for this app.

### Where is the -sources version
Deprecated. At least for now...

### Support for more OSes? 
See TODO
