### [Main branch](https://github.com/P-OEM/P-OEM-s-void-setup/tree/main)

# Bluetooth setup

### this branch contain a simple guide for setting up bluetooth in a xfce, void linux system, with bluez and blueman

## [Bluetooth introduction](#introduction)
## [Bluez setup with Runit](#bluez-setup)
## [Bluman start](#blueman)
## [Blue-man do I have to do this part?](#disable-the-blueman-bluetooth-startup)

## Introduction
* there are some different alternatives available for setting up bluetooth on a void system, but in this guide, the tools will be `bluez` with `blueman`
    * `bluez`
        * `bluez` contain bluetooth tools and daemons
    * `blueman`
        * `blueman` is a bluetooth manager, that also work together with `bluez`
        * `blueman` bring a nice graphical interface for the user
* for this guide it's expected that both blues package, and `blueman` package is installed
* here are two links for some resources
    * here's a video from youtube for how to do this setup on an Arch system [youtube video](https://youtu.be/b329S-LFV0k)
        * keep in mind that the path `/etc/runit/sv` will be `etc/sv` on the void system
    * here is the link documenting the sv path [services and daemons](https://docs.voidlinux.org/config/services/index.html) (void documentation)
        * look for the `Enabling Services` title

## Bluez setup
* `bluez` come with a daemon that `Runit` (the init service), will have to start when the operating system starts
* this can be done by linking it to the runsvdir
    * paste this into the terminal `ln -s /etc/sv/bluetoothd /etc/runit/runsvdir/default`
## Blueman
* blueman does not really need any setup
    * type:
        * `blueman-manager`
    * into the terminal and hit enter
        * say yes to automatic bluetooth enabling and you're good to go...

## Disable the blueman bluetooth startup
* this is actually simple, but it's not intuitive
* now go to:
    * settings manager (settings)
        * Session and startup
            * Application Autostart
                * `+Add`
                * then fill inn and pick
                    * Name = `bluetooth disabler`
                    * Description = `disable blueman autostart of bluetooth`
                    * Command = `bluetoothctl power off`
                    * Trigger = `on login`
                        * then click ok and reboot to see that bluetooth no longer is on when you start
