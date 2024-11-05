# SDL 1.2 PAX

***Beware: this modification is not done properly and might annoy anyone with real programming knowledge***

SDL-1.2 fork with necessary modifications for PAX terminals and ProlinOS
Includes halfassed keypad support and touchscreen (mouse emulation) support

Build info:
* requires correctly set paths to arm-2012.03 toolchain
* `./configure --host=arm-none-linux-gnueabi`
* `make`

and pushing:
* `python3 <prolin-xcb-client/client.py> <tty> push build/.libs/libSDL-1.2.so.0.11.5 /data/app/MAINAPP/lib/libSDL-1.2.so.0`

Usage in ports:
```c
SDL_putenv("SDL_VIDEODRIVER=fbcon");
SDL_putenv("SDL_FBDEV=/dev/fb");
SDL_putenv("SDL_AUDIODRIVER=dsp");
SDL_putenv("SDL_PATH_DSP=/dev/snd/dsp");
```

# DEPRECATED

The 1.2 branch of SDL is deprecated. While we occasionally collect fixes
in revision control, there has not been a formal release since 2012, and
we have no intention to do future releases, either.

Current development is happening in SDL 2.0.x, which gets regular
releases and can be found at:

https://github.com/libsdl-org/SDL

Thanks!



# Simple DirectMedia Layer (SDL) Version 1.2

https://www.libsdl.org/

This is the Simple DirectMedia Layer, a general API that provides low
level access to audio, keyboard, mouse, joystick, 3D hardware via OpenGL,
and 2D framebuffer across multiple platforms.

The current version supports Linux, Windows CE/95/98/ME/XP/Vista, BeOS,
MacOS Classic, Mac OS X, FreeBSD, NetBSD, OpenBSD, BSD/OS, Solaris, IRIX,
and QNX.  The code contains support for Dreamcast, Atari, AIX, OSF/Tru64,
RISC OS, SymbianOS, Nintendo DS, and OS/2, but these are not officially
supported.

SDL is written in C, but works with C++ natively, and has bindings to
several other languages, including Ada, C#, Eiffel, Erlang, Euphoria,
Guile, Haskell, Java, Lisp, Lua, ML, Objective C, Pascal, Perl, PHP,
Pike, Pliant, Python, Ruby, and Smalltalk.

This library is distributed under GNU LGPL version 2, which can be
found in the file  "COPYING".  This license allows you to use SDL
freely in commercial programs as long as you link with the dynamic
library.

The best way to learn how to use SDL is to check out the header files in
the "include" subdirectory and the programs in the "test" subdirectory.
The header files and test programs are well commented and always up to date.
More documentation is available in HTML format in "docs/index.html".

The test programs in the "test" subdirectory are in the public domain.

Enjoy!

Sam Lantinga (slouken@libsdl.org)

