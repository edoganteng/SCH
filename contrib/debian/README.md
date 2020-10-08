
Debian
====================
This directory contains files used to package schillingcoind/schillingcoin-qt
for Debian-based Linux systems. If you compile schillingcoind/schillingcoin-qt yourself, there are some useful files here.

## schillingcoin: URI support ##


schillingcoin-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install schillingcoin-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your schillingcoin-qt binary to `/usr/bin`
and the `../../share/pixmaps/schillingcoin128.png` to `/usr/share/pixmaps`

schillingcoin-qt.protocol (KDE)

