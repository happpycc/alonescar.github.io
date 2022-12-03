---
title: Archlinux Desktop Install
date: 2022-11-30 21:57:01
tags:
  - Archlinux
categories:
  - System
---

For alonescar, the desktop system he choose is `dwm`.
`dwm` is based on `xorg` and there are some based tools need to be downloaded, such as `dmenu`, `slstatus`, `st` and so on.

## Install `xorg`
```
sudo pacman -S xorg xorg-xinit udisk2 udiskie
```

## Download `dwm` and some neccessary tools

* [st](https://st.suckless.org/) A simple terminal
* [dmenu](https://tools.suckless.org/dmenu/) A menu which is put the top of the window by default, you can search by it.
* [slstatus](https://tools.suckless.org/slstatus/) A status bar

<!--more-->

alonescar hope install in a folder like `Softwares`, it will be more easy to manage.

```
git clone https://git.suckless.org/dwm
git clone https://git.suckless.org/st
git clone https://git.suckless.org/dmenu
git clone https://git.suckless.org/slstatus
```

## Installation

Enter the root directory of each project and install it, as shown below.

```
cd dwm
sudo make clean install
```

The four project were created by the same company named `suckless`, so they can be together

## Configure
### Copy `.xinitrc` to home
```
cp /etc/X11/xinit/xinitrc ~/.xinitrc
```

To add some startup items into `~/.xinitrc` file, it will be runned after xorg init

### Add `dwm` into `.xinitrc`
```
nvim ~/.xinitrc
exec dwm
```
Add `exec dwm` to end of fild

## Run `startx`
The basic desktop system is installed, you can run `startx` to start it.
