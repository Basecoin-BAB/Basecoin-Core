
Debian
====================
This directory contains files used to package basecoind/basecoin-qt
for Debian-based Linux systems. If you compile basecoind/basecoin-qt yourself, there are some useful files here.

## basecoin: URI support ##


basecoin-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install basecoin-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your basecoin-qt binary to `/usr/bin`
and the `../../share/pixmaps/basecoin128.png` to `/usr/share/pixmaps`

basecoin-qt.protocol (KDE)

