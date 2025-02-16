### [Main branch](https://github.com/P-OEM/P-OEM-s-void-setup)

# GNOME keyring setup

### this branch contain a simple guide for setting up GNOME keyring in a xfce, void linux system

## [GNOME keyring introduction](#introduction)
## [GNOME keyring startup](#startup)

## Introduction
* it is expected that `gnome-keyring` and `libsecret` packages are installed before using this guide
* in this guide you will be able to set up the GNOME keyring service in such a way that you log into your keyring storing passwords for services on your account, when you log in.
* this guide use cli and text manipulators or editors only

## Startup
* open your terminal, pick your favorite text program and edit the file `/etc/pam.d/login` as superuser
    * example with neovim:
        ```sh
        sudo nvim /etc/pam.d/login
        ```
    * then add these lines:
        ```sh
        # login gnome-keyring on startup
        auth       optional     pam_gnome_keyring.so
        session    optional     pam_gnome_keyring.so auto_start
        ```
* if you're using `LightDM` do the same to `/etc/pam.d/lightdm`
    * example with neovim:
        ```sh
        sudo nvim /etc/pam.d/lightdm
        ```
    * then add these lines:
        ```sh
        # login gnome-keyring on startup
        auth       optional     pam_gnome_keyring.so
        session    optional     pam_gnome_keyring.so auto_start
        ```
