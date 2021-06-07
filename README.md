# budgie-extras-voidlinux
Void Linux Template for compiling budgie-extras package, additional applets for Budgie desktop to enhance user experience. Ported from Ubuntu Budgie.

<H1>Included applets</H1>

## Plugins:

 - Hotcorners
 - Quicknote
 - Workspace Switcher Overview
 - Wallpaper Switcher
 - Workspace Mover
 - ShowTime
 - CountDown
 - Automatic Keyboard Layout Switcher
 - Screen Rotation Lock
 - ClockWorks
 - DropBy
 - Kangaroo
 - WeatherShow
 - Trash
 - App-launcher
 - RecentlyUsed
 - Take-A-Break
 - Workspace Stopwatch
 - Fuzzy Clock
 - Brightness Controller
 - Visualspace
 - Applications Menu
 - Network Manager

## Standalone

budgie mini-apps - see the individual components for details

 - Budgie Extras Daemon
 - Budgie Wallstreet
 - Budgie Quickchar (needs the extras daemon as a runtime dependency)
 - Budgie Window Previews (needs the extras daemon as a runtime dependency)
 - Budgie Shuffler (needs the extras daemon as a runtime dependency)

<H1>How to install</H1>

 <H2>Building from template</H2>

First of all, we'll need xtools installed in order to use properly xbps-src:

     sudo xbps-install xtools

If you haven't cloned the <code>void-packages</code> repository already, do it now:

     git clone --depth=1 https://github.com/void-linux/void-packages

Prepare the build environment (do this once if not done already):

     cd void-packages
     ./xbps-src binary-bootstrap

Clone the template to <code>srcpkgs</code> directory, compile it and install:

     git clone https://github.com/KF-Art/budgie-extras-voidlinux/ && cd budgie-extras-voidlinux
     cp -r budgie-extras ../srcpkgs/ && cd ..
     ./xbps-src pkg budgie-extras # compile the package
     xi budgie-extras # install the package
  
This template uses the official release from Ubuntu Budgie repository.

 <H2>Installing precompiled binary</H2>
There is also an binary package to install directly to your system. I recommend this if you don't want to go through the building process, but this may be outdated sometimes. I'll try to mantain this updated as is possible for me.


To install it, just do the following steps:

     git clone https://github.com/KF-Art/budgie-extras-voidlinux
     cd budgie-extras-voidlinux/bin/ 
     xbps-rindex -a *.xbps
     sudo xbps-install --repository=$PWD budgie-extras
