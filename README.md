# dwm - dynamic window manager
## dwm is an extremely fast, small, and dynamic window manager for X.


### Requirements

In order to build dwm you need the Xlib header files.

### Changes

* Changed hotkeys
* "make clean" command deletes config.h
* Changed color scheme
* Support for readiness notification file descriptor

### Patches

* [layoutscroll](https://dwm.suckless.org/patches/layoutscroll/)
* [resizecorners](https://dwm.suckless.org/patches/resizecorners/)
* [removeborder](https://dwm.suckless.org/patches/removeborder/)
* [hide vacant tags](https://dwm.suckless.org/patches/hide_vacant_tags/)
* [fibonacci](https://dwm.suckless.org/patches/fibonacci/) (only dwindle layout)
* [gridmode](https://dwm.suckless.org/patches/gridmode/)
* [anybar-polybar](https://github.com/mihirlad55/dwm-anybar)
* [dwm-ipc](https://github.com/mihirlad55/dwm-ipc)
* [alpha/fixborders](https://dwm.suckless.org/patches/alpha/)

### Polybar

This dwm build uses [polybar-dwm-module](https://github.com/mihirlad55/polybar-dwm-module).

Check out my [dotfiles](https://github.com/Senderman/dotfiles/tree/master/polybar/.config/polybar) repo to see how to configure polybar


### Installation

Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if
necessary as root):

`make clean install`


### Running dwm

Add the following line to your .xinitrc to start dwm using startx:

`exec dwm`

### Configuration

The configuration of dwm is done by modifying config.def.h
and (re)compiling the source code.
