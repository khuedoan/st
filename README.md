# st - simple terminal

st is a simple terminal emulator for X which sucks less.

![Screenshot](https://i.imgur.com/HtHdlPu.png)

# Requirements

In order to build st you need the Xlib header files.

# Installation

Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

```sh
make clean install
```

# Running st

If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

```sh
tic -sx st.info
```

See the man page for additional details.

# Blur effect

This fork leverages picom's new kawase blur method instead of taking a screenshot, blur it using ImageMagick without hardware acceleration and then set it as the lock screen wallpaper.
The end result is much higher performance and much lower latency.
Currently, you will need to enable the experimental backend in picom using `picom --experimental-backends`, you can check out my picom config [here](https://github.com/khuedoan/dotfiles/blob/master/.config/picom/picom.conf#L29).

# Credits

Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.
