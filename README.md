### [Main branch](https://github.com/P-OEM/P-OEM-s-void-setup)

# Date and time setup

### this branch contain a simple guide for setting up a network time protocol with chrony on a void linux system

## [Date and time setup introduction](#introduction)
## [Date and time setup using the chrony package](#using-the-chrony-package)
## [Date and time setup syncronise hardware clock](#syncronise-hardware-clock)

## Introduction
* it is expected that the `chrony` package is installed before using this guide
* the standard way of syncronising time on a device is with ntp (network time protocol)
    * chrony is an ntp
* now, ntp can help you syncronise time when your system is connected to the internet
    * however, the computer also have an internal hardware clock
        * the hardware clock can be syncronise with chrony or other ntp protocols
* for more options, and information see the official void linux documentation for it [here](https://docs.voidlinux.org/config/date-time.html)

## Using the chrony package
* to activate the chrony daemon (background service), run:
```sh
sudo ln -s /etc/sv/chronyd /var/service
```
* then reboot

## Syncronise hardware clock
* to syncronise hardware clock open `/etc/rc.conf` as super user with text editor of your choice
    * example:
    ```
    sudo nvim /etc/rc.conf
    ```
* the add this line
`HARDWARECLOCK="localtime"`
