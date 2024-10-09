### [Main branch](https://github.com/P-OEM/P-OEM-s-void-setup/tree/main)

# brightnessctl
### this branch contains a simple guide for setting the default screen brightness with brightnessctl and runit init service

## [brightnessctl introduction](#introduction)
## [brightnessctl current brightness](#using-brightnessctl-to-set-current-brightness) 
## [brightnessctl default brightness](#using-brightnessctl-to-set-default-brightness)

## Introduction
* for this guide it's expected that the `brightnessctl` package is installed
* this guide will use some of the `brightnessctl` packages commands, and combine it with the init service `runit` through the `/etc/rc.local` file, to set the brightness whenthe computer starts.
* for more information on `brightnessctl`, I recommend reading the programs github page [here](https://github.com/Hummer12007/brightnessctl)

## Using brightnessctl to set current brightness
* run `brightnessctl i` to see the current screen brightness percentage and value
    * now change the value with percentage by running `brightnessctl s ThePercentageYouWant%`
    * now run `brightnessctl i` again to see the change in values

## Using brightnessctl to set default brightness
* use your favorite text editor or text manipulator (like vim), to add the line `brightnessctl s ThePercentageYouWant%` to the file `/etc/rc.local`
* on system start the line will be run by `runit`, and make brightnessctl set `ThePercentageYouWant%` as the brightness level on your systems screen.
