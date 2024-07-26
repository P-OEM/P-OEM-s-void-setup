# void-linux-setup

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

## [Launcher setup]()
</details>

<details>
<summary>Specific tool setup README file links</summary>

## [Brightnessctl default screenbrightness setup]()
## [Bluetooth setup]()
## [Themes setup]()
## [Background image setup]()
## [Neovim setup]()
## [LibreOffice setup]()
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

* void-repo-nonfree (allow nonfree packages on the system)
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
