# P-OEM's void linux setup

## About this setup
* it is a public version of my personal setup, meaning that it's not the same, but it contains a lot of smaller installation guides, and packages I've installed to shape my system to my needs

* this does not have an install guide (yet). for that I recomend the official installation guide [here](https://docs.voidlinux.org/installation/index.html) or this youtube video [here](https://youtu.be/wiP38mNXujE), the same youtuber have an installation guide for the `musl` library version as well

* I've been using the `xfce` `glibc` version of Void linux, and this setup is shaped around that
    * that doesn't mean that some of the solutions can't be applied to other systems to, but they may not work

* for the most part this setup should be self explanatory, read the titles

## titles with links:
<details>
<summary>Local branch titles</summary>

## [xfce desktop environment settings](#xfce-settings)
## [xbps package manager packages](#xbps-packages)
## [npm package manager packages](#npm-packages)
## [gem package manager packages](#gem-packages)
</details>

<details>
<summary>General setup README file links</summary>

## [General solutions to issues](https://github.com/P-OEM/P-OEM-s-void-setup/tree/general-solutions)
## [Launcher setup](https://github.com/P-OEM/P-OEM-s-void-setup/tree/launcher)
</details>

<details>
<summary>Specific tool setup README file links</summary>

## [Git setup](https://github.com/P-OEM/P-OEM-s-void-setup/tree/git)
## [AppArmor setup](https://github.com/P-OEM/P-OEM-s-void-setup/tree/apparmor?tab=readme-ov-file)
## [Brightnessctl default screenbrightness setup](https://github.com/P-OEM/P-OEM-s-void-setup/tree/brightnessctl-default-screenbrightness-setup)
## [Bluetooth setup](https://github.com/P-OEM/P-OEM-s-void-setup/tree/bluetooth)
## [Themes setup](https://github.com/P-OEM/P-OEM-s-void-setup/tree/themes)
## [Background image setup](https://github.com/P-OEM/P-OEM-s-void-setup/tree/background-image)
## [Neovim setup](https://github.com/P-OEM/P-OEM-s-void-setup/tree/neovim)
## [LibreOffice setup](https://github.com/P-OEM/P-OEM-s-void-setup/tree/libreoffice)
## [Thunderbird setup](https://github.com/P-OEM/P-OEM-s-void-setup/tree/thunderbird)
## [Discord setup](https://github.com/P-OEM/P-OEM-s-void-setup/tree/discord)
## [Skype setup](https://github.com/P-OEM/P-OEM-s-void-setup/tree/skype)
## [Docker setup](https://github.com/P-OEM/P-OEM-s-void-setup/tree/docker)
## [Veloren setup](https://github.com/P-OEM/P-OEM-s-void-setup/tree/veloren)
## [Steam](https://github.com/P-OEM/P-OEM-s-void-setup/tree/steam)
* [Proton list](https://github.com/P-OEM/P-OEM-s-void-setup/tree/proton)
</details>

## xfce settings
### This section cover settings under settings manager, the settings are grouped under their category title
<details>
<summary>Appearance</summary>

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
* Advanced
    * Shortcuts
        * Disable menu shortcut key (F10 by default) = on
</details>

<details>
<summary>Mouse and Touchpad</summary>

* Devices
    * Touchpad
        * Tap touchpad to click = off
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
* cowsay
* fortune-mod
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
* nvtop
</details>

<details>
<summary>security</summary>

* apparmor
</details>

<details>
<summary>zip packages</summary>

* thunar-archive-plugin
* xarchiver
* unzip
* xz
</details>

<details>
<summary>programming packages</summary>

* git
* github-cli
* curl
* neovim
* gcc
* make
* cmake
* ruby
* ruby-devel
* pnpm
* docker
</details>

<details>
<summary>Language servers</summary>

* clang
* clang-tools-extra
* lua-language-server
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
* libreoffice-i18n-en-US
* libreoffice-i18n-nb
</details>

<details>
<summary>cloud storage</summary>

* dropbox (run `dropbox update` in terminal after install)
</details>

<details>
<summary>graphics packages</summary>

* mesa-vulkan-intel (works for intel cpu graphics)
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
### more information from video ([here](https://youtu.be/QhOr5ucywtU))
* the original page wiki page is no longer available
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
