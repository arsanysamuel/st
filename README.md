# **st** - simple terminal

This is my build of the [suckless st](https://st.suckless.org/) version 0.9, including extra configuration and applied patches.

**st** is a simple terminal emulator for X which sucks less.


## Requirements

In order to build st you need the Xlib header files.

Make sure you've installed a C compiler and `make` utility, for Arch Linux install `base-devel`.


## Installation

Edit `config.mk` to match your local setup (st is installed into
the `/usr/local` namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

```
# make clean install
```

See the [st](https://st.suckless.org/) official webpage or the [st archwiki page](https://wiki.archlinux.org/title/St).


## Configuration

The configuration of st is done by creating a custom `config.h` (a copy of `config.def.h`) and (re)compiling the source code.


## Running st

If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

```
tic -sx st.info
```

See the man page for additional details.


## Credits

Based on [Aurélien APTEL](mailto:aurelien.aptel@gmail.com) bt source code.


## Patches

These are the [patches](https://st.suckless.org/patches/) that I've applied to my build:
- [alpha](http://st.suckless.org/patches/alpha/st-alpha-20220206-0.8.5.diff)
