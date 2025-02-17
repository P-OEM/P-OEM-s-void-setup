### [Main branch](https://github.com/P-OEM/P-OEM-s-void-setup)

# Keyboard language

### this branch contain a simple guide for setting up Keyboard language in a xfce, void linux system

## [Keyboard language introduction](#introduction)
## [Keyboard language startup](#startup)

## Introduction
* in this guide you will be able to set up the keyboard language before you log in to your system
* this guide use cli and text manipulators or editors only

## Startup
* open your terminal, make `/etc/lightdm/lightdm.conf` directory if it doesn't exist
    ```sh
    sudo mkdir /etc/X11/xorg.conf.d
    ```
    * pick your favorite text program and edit/ make the file `/etc/X11/xorg.conf.d/00-keyboard.conf` as superuser
        * example with neovim:
            ```sh
            sudo nvim /etc/X11/xorg.conf.d/00-keyboard.conf
            ```
    * then add these lines and replace `"en"` with your keyboards language:
        ```sh
        Section "InputClass"
            Identifier "system-keyboard"
            MatchIsKeyboard "on"
            Option "XkbLayout" "en"  # set language for keyboard before login (en, fr, de)
        EndSection
        ```
