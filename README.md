# gamingtruble's void linux setup

## About this setup
* it is a public version of my personal setup, meaning that it's not the same, but it contains a lot of smaller installation guides, and packages I've installed to shape my system to my needs

* this does not have an install guide (yet). for that I recomend the official installation guide [here](https://docs.voidlinux.org/installation/index.html) or this youtube video [here](https://youtu.be/wiP38mNXujE), the same youtuber have an installation guide for the musl library version as well

* I've been using the `xfce` `glibc` version of Void linux, and this setup is shaped around that
    * that doesn't mean that some of the solutions can't be applied to other systems to, but they may not work

* for the most part, this setup should be self explanatory by reading the titles

<details>
<summary>quick start</summary>

* to use this setup repository efficiently, I recommend first looking at the packages, pick what you want/ need and then look to the `Specific too setup README file links`
    * if you're anything like me, and have good vision, but don't know how to use it, then I recommend hitting `ctrl` + `f` and search for the words `xbps`, and when you're done looking at packages, search `specific`
        * if you're even more like me, and a bit used to windows behaviour, you might want to have a look at the `xfce settings` part before you move on to the `Specific too setup README file links`
</details>

<details>
<summary>Expected questions</summary>

* why make it public?
    * I've seen a lot of people have some of the same issues as me, so it seems like a good way to help out
    
* what are you keeping away from us in your private repo?
    * I'm sorry, I'm keeping my Neovim setup, wallpaper, theme and unfinished branches to myself

* is it advanced?
    * no it's not, as I'm not a very advanced linux user. this guide will mostly help out if you happen to be completely stuck on something simple, like getting steam to run and get rid of that pesky can't find `libc.so.6` issue
</details>

## titles with links:
<details open> 
<summary>Local branch titles</summary>

## [xfce desktop environment settings](#xfce-settings)
## [xbps package manager packages](#xbps-packages)
## [npm package manager packages](#npm-packages)
## [gem package manager packages](#gem-packages)
</details>

<details>
<summary>General setup README file links</summary>

## [Launcher setup](https://github.com/gamingtruble/gamingtruble-s-void-setup/tree/launcher)
</details>

<details>
<summary>Specific tool setup README file links</summary>

## [Brightnessctl default screenbrightness setup](https://github.com/gamingtruble/gamingtruble-s-void-setup/tree/brightnessctl-default-screenbrightness-setup)
## [Bluetooth setup](https://github.com/gamingtruble/gamingtruble-s-void-setup/tree/bluetooth)
## [Themes setup](https://github.com/gamingtruble/gamingtruble-s-void-setup/tree/themes)
## [Background image setup](https://github.com/gamingtruble/gamingtruble-s-void-setup/tree/background-image)
## [Neovim setup](https://github.com/gamingtruble/gamingtruble-s-void-setup/tree/neovim)
## [LibreOffice setup](https://github.com/gamingtruble/gamingtruble-s-void-setup/tree/libreoffice)
## [Thunderbird setup]()
## [Discord setup]()
## [Skype setup]()
## [Veloren setup]()
</details>

## xfce settings
### This section cover settings under settings manager, the settings are grouped under their respectable category title
<details>
<summary>Appearance</summary>

* Style  
    * Fantasma-Solid (require theme)
* Icons
    * candy-icons (require icon themes)
* Fonts   
    * Sans Regular
        * Size = 11
    * Sans Monospace Regular
        * Size = 11
</details>

<details>
<summary>WindowManager</summary>

* Keyboard
    * Maximize window = f11
    * Toggle fullscreen = Ctrl+f11
    * Move window to left workspace = Shift+Ctrl+Alt+Left
    * Move window to right workspace = Shift+Ctrl+Alt+right
    * Tile window to the top = Super+Up
    * Tile window to the bottom = Super+Down
    * Tile window to the left = Super+Left
    * Tile window to the right = Super+Right
    * Tile window to the top-left = Super+H
    * Tile window to the top-right = Super+K
    * Tile window to the bottom-left = Super+J
    * Tile window to the bottom-right = Super+L
</details>

<details>
<summary>WindowManager Tweaks</summary>

* Accessibility
    * Automatically tile windows when moving toward the screen edge = on
</details>

<details>
<summary>Terminal Preferences</summary>

* Appearance
    * Font
        * Terminus Bold 14
    * Background
        * Transparent Background
            * Opacity = 0.70
</details>

<details>
<summary>Mouse and Touchpad</summary>

* Devices
    * Touchpad
        * Tap touchpad to click = off
* Theme
    * ArcAurora Cursors (require pointer theme)
</details>

<details>
<summary>Keyboard</summary>

* Application Shortcuts
    * xkill = Ctrl+Escape
</details>

## xbps packages
<details>
<summary>funny packages</summary>

* sl
* cmatrix
</details>

<details>
<summary>helpfull</summary>

* void-repo-nonfree (allow nonfree packages on the system, needed for steam)
* void-repo-multilib (add 32 bit packages, needed for steam)
* bash-completion
* xkill
* brightnessctl
* xreader (document viewer, pdf)
* screenFetch
* xfce4-screenshooter
* noto-fonts-emoji
* ttf-ubuntu-font-family
* gnome-disk-utility
* galculator
</details>

<details>
<summary>zip packages</summary>

* thunar-archive-plugin
* xarchiver
* unzip
* xz
</details>

<details>
<summary>bluetooth packages</summary>

* bluez
* blueman
</details>

<details>
<summary>e-mail</summary>

* thunderbird
</details>

<details>
<summary>office packages</summary>

* libreoffice
* libreoffice-writer
* libreoffice-impress
* libreoffice-calc
* libreoffice-math
* libreoffice-base
* libreoffice-i18n-en
* libreoffice-i18n-nb
</details>

<details>
<summary>graphics packages</summary>

* mesa-vulkan-intel (works for cpu graphics)
* mesa-vulkan-radeon (works for amd graphics card)
* gimp
* blender
* krita
* kdenlive
</details>

<details>
<summary>book library packages</summary>

* calibre
</details>

<details>
<summary>programming packages</summary>

* git
* github-cli
* curl
* neovim
* gcc
* g++
* make
* cmake
* ruby
* ruby-devel
* pnpm
</details>

<details>
<summary>Language servers</summary>

* clang
* clang-tools-extra
* lua-language-server
</details>

<details>
<summary>voice chat</summary>

* skype
</details>

<details>
<summary>games</summary>

* dwarffortress
* minetest
* supertux2
* supertuxkart
</details>

<details>
<summary>steam</summary>

* steam
### open source drivers (mesa drivers)
* libgcc-32bit 
* libstdc++-32bit
* libdrm-32bit
* libglvnd-32bit
* mesa-dri-32bit
### more information ([here](https://wiki.voidlinux.org/voidlinux_en_all_2021-04/A/Steam))
</details>

## npm packages
* require npm package installed
* for this package manager commands are shown

<details>
<summary>Typescript Language Server</summary>


* `sudo npm install -g typescript-language-server typescript`
</details>

## gem packages
* require ruby and the ruby devel package installed (the ruby package contain the gem package as well)
* for this package manager commands are shown

<details>
<summary>Ruby gem packages</summary>

* `gem install solargraph` (ruby language server)
</details>

* after this installation, you probably need to add the user directory to the system path
    * this can be done by piping an `echo` command of the path into your users home directory, then to `.bashr` like this
        * `echo 'export PATH=$PATH:/add/the/path/that/the/installation/says/is/missing/from/the/path/here' >> ~/.bashrc`
