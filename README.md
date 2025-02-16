### [Main branch](https://github.com/P-OEM/P-OEM-s-void-setup)

# PlatformIO install

### this branch contain a simple guide for installing and setting up PlatformIO

## [PlatformIO introduction](#introduction)
## [PlatformIO installation](#installation)
## [PlatformIO allow user to upload code to arduino device](#allow-user-to-upload-code-to-arduino-device)

## Introduction
* PlatformIO tldr:
    * embeded IO platform

## installation
* go to the PlatformIO [webpage](https://platformio.org/)
* click on `PlatformIO Core (CLI)` menu option at the bottom of the page under `Solutions` title
* click on `>_ PlatformIO Core` button
* click on `Installer Script (Recommended)` option
* click on `Local Download (macOS / Linux / Windows)` option
* click on `get-platformio.py` link
    * take the text from `get-platformio.py` link, and add it to `~/platformio/get-platformio.py` file
        * `~` means home directory (folder)
        * `.py` is a python file extension
            * go to `~/platformio` then run the command:
            ```sh
            python get-platformio.py
            ```
* install shell commands
    * got to home folder `~`
        * open `.bashrc` with a text editor or manipulator
            * add this line to the bottom of the file
                * `export PATH=$PATH:$HOME/.platformio/penv/bin`
                    * this will add `.platformio/penv/bin` from the home folder to the path
## allow user to upload code to arduino device
* run this command
* `curl -fsSL https://raw.githubusercontent.com/platformio/platformio-core/develop/platformio/assets/system/99-platformio-udev.rules | sudo tee /lib/udev/rules.d/99-platformio-udev.rules`
