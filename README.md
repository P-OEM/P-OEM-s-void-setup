### [Main branch](https://github.com/P-OEM/P-OEM-s-void-setup/tree/main)

# Bluetooth setup

### this branch contain a simple guide for setting up bluetooth in a xfce, void linux system, with bluez and blueman

## [Bluetooth introduction](#introduction)
## [Bluez setup with Runit](#bluez-setup)
## [Bluetooth rfkill unblocking](#unblock-bluetooth)
## [Dbus setup](#dbus-service-setup)
## [Audio device xbps packages](#audio-device-support)
## [File sharing xbps package](#file-sharing-support)
## [Bluman start](#blueman-setup)
## [Blueman dissable on startup](#disable-the-blueman-bluetooth-startup)

## Introduction
* it's expected that the `bluez`, `blueman`, and the `dbus` service packages are installed for this guide
    * `bluez`
        * `bluez` contain bluetooth tools and daemons
    * `blueman`
        * `blueman` is a bluetooth manager, that also work together with `bluez`
        * `blueman` bring a nice graphical interface for the user
        * `dbus` service, a message bus (handle data sent between programs)
* here are two links for some resources
    * you can find the official void linux bluetooth documentation [here](https://docs.voidlinux.org/config/bluetooth.html)

## Bluez setup
* `bluez` come with a daemon that `Runit` (the init service), will have to start when the operating system starts
* this can be done by linking it to the runsvdir
    * paste this into the terminal `ln -s /etc/sv/bluetoothd /etc/runit/runsvdir/default`

## Unblock bluetooth
* make sure rfkill is not blocking bluetooth
    * paste `rfkill` into terminal for block list
    * paste `rfkill unblock bluetooth` to unblock bluetooth

## dbus service setup
* if dbus isn't installed and running you might have to either start it or set it up to run
    * see if it's running (status is first word)
        * `sudo sv status dbus`
    * making it run
        * `sudo sv up dbus`
    * linking it to runsvdir to start with OS
        * paste this into the terminal `ln -s /etc/sv/dbus /etc/runit/runsvdir/default`
* add your user to the dbus group
    * paste this into terminal, remember to change username to your users username
        * `sudo usermod -aG bluetooth username`
* I recommend restarting your system/ PC at this point

## Audio device support
* PipeWire support package
    * `libspa-bluetooth`
* ALSA support package
    * `bluez-alsa`
* PulseAudio
    * no need for seperate packages

## File sharing support
* Bluetooth tools and daemons - obex OBject EXchange package
    * `bluez-obex`

## Blueman setup
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
