### [Main branch](https://github.com/gamingtruble/gamingtruble-s-void-setup)

# AppArmor setup
### this branch contains a simple guide for setting up the AppArmor kernel security module void linux system with grub

## [AppArmor introduction](#introduction)
## [AppArmor configuration](#configuration)
## [AppArmor kernel commandline commands](#kernel-commandline-commands)

## Introduction
* it is expected that the AppArmor package are installed before following the steps in this guide
* setting up the AppArmor can be done in two steps
    * 1. setting the configuration for AppArmor
    * 2. adding the AppArmor commands in the grub configuration file
* this guide will be using vim, but you can pick your favourite text editor and use that instead

* source links
    * the AppArmor website [https://apparmor.net/](https://apparmor.net/)
    * an incredibly usefull youtube video, covering the practical part of this guide [here](https://youtu.be/H7b3yfIyva0)
    * the void linux AppArmor documentation [here](https://docs.voidlinux.org/config/security/apparmor.html)
## Configuration
* the AppArmor configuration have three options found in the apparmor file
    * `disable`, `complain`, `enforce`
    * these can be set by uncommenting (remove the `#`) `APPARMOR=disable`
        * you can set `APPARMOR=` and the option you want (probably `enforce` if you actually want AppArmor to be used)

* to configure AppArmor, open the AppArmor configuration file as super user
    * this can be done with vim, by typing this in the terminal:
        * `sudo vim /etc/default/apparmor`
            * the file would look like this for the enforce option
            ```bash
            # Possible options:
            # - disable
            # - complain
            # - enforce
            APPARMOR=enforce
            ```

## Kernel commandline commands
* to make your system use AppArmor, you will have to add two commands to the kernel commandline

* on a system using grub this can be done by opening the configuration file for grub and adding `apparmor=1` and `security=apparmor` commands to `GRUB_CMDLINE_LINUX_DEFAULT`
     * this again can be done with vim, by typing this in the terminal:
        * `sudo vim /etc/default/grub`
            * the files content should look like this when you're done
            ```bash
            #   
			# Configuration file for GRUB.
			#
			GRUB_DEFAULT=0
			#GRUB_HIDDEN_TIMEOUT=0
			#GRUB_HIDDEN_TIMEOUT_QUIET=false
			GRUB_TIMEOUT=5
			GRUB_DISTRIBUTOR="Void"
			GRUB_CMDLINE_LINUX_DEFAULT="loglevel=4 apparmor=1 security=apparmor"
			# Uncomment to use basic console
			#GRUB_TERMINAL_INPUT="console"
			# Uncomment to disable graphical terminal
			#GRUB_TERMINAL_OUTPUT=console
			#GRUB_BACKGROUND=/usr/share/void-artwork/splash.png
			#GRUB_GFXMODE=1920x1080x32
			#GRUB_DISABLE_LINUX_UUID=true
			#GRUB_DISABLE_RECOVERY=true
			# Uncomment and set to the desired menu colors.  Used by normal and wallpaper
			# modes only.  Entries specified as foreground/background.
			#GRUB_COLOR_NORMAL="light-blue/black"
			#GRUB_COLOR_HIGHLIGHT="light-cyan/blue"
            ```

