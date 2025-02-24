### [Main branch](https://github.com/P-OEM/P-OEM-s-void-setup)

# Signal setup
### this branch contains a simple guide for setting up signal in a void linux system with the xfce desktop environment

## [Signal about this guide](#about-this-guide)
## [Signal start on login](#start-on-login)

## About this guide
* it is expected that the packages for `Signal-Desktop` installed before following this guide
* for the most part signal just works, and guide the user through how to set it up
    * this guide simply cover how to run it when loging into the system
* source for some of this information... [Reddit](https://www.reddit.com/r/signal/comments/lcpo4e/protip_for_new_users_add_startintray_to_your/) XD

## Start on login
* go to
    * `xfce4-settings-manager`
        * `Session and Startup`
            * `Application Autostart`
* click
    * `+Add`
        * in the Add application window:
            * `Name`:
                ```sh
                Signal-Desktop
                ```
            * `Description:`
                ```sh
                Start signal
                ```
            * `Command:`
                ```sh
                signal-desktop
                ```
            * `Trigger:`
                ```sh
                on login
                ```

* options
    * you can add ` --start-in-tray` to the end of the command to make signal start as an icon on your menu bar
    * you can add ` --use-tray-icon` to the end of the command to make signal start as a window with an icon on your menu bar
    * you can also set these as settings from
        * `File`
            * `Preferences…`
                * `General`
                    * `System`
