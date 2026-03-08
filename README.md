### [Main branch](https://github.com/P-OEM/P-OEM-s-void-setup)

# Zotero setup
### this branch contains a simple guide for setting up zotero in a void linux system with the xfce desktop environment

## [Zotero about this guide](#about-this-guide)
## [Zotero download tarball](#download-tarball)
## [Zotero unzip](#unzip)
## [Zotero shortcut](#shortcut)

## About this guide
* it is expected that the packages for ziping and unziping are installed before following the steps in this part of the void linux setup
* zotero is a free tool to help you site sources.
    * for more information I reccomend visiting their [site](https://www.zotero.org/)
    * i also reccomend watching [this video](https://youtu.be/tnbwKj6-pD8?list=PLhLBstyv76b9rTqPsszF1NJh5uQv8xRB8) on youtube, if you need an introduction to setting up more, and using the program
* the terminal is not needed for this guide
* if you want to make a launcher, you can do the unzip part of this guide, then go to the [launcher](https://github.com/P-OEM/P-OEM-s-void-setup/tree/launcher) branch
    * the launcher should contain:
    ```cmd
    [Desktop Entry]
    Name=zotero
    Path=/home/user
    Exec=insert_unzipedfolder_name/zotero
    Icon=zotero.ico
    Type=Application
    Categories=Office;
    ```

## Download tarball
* to install Zotero on the void linux system, you can grab the tarball download from the official [Zotero website](https://www.zotero.org/) under the download section
    * download the 64 bit version for linux

## Unzip
* now that the tarball is downloaded, I would recommend moving it to the home folder of your user (~). You can then unzip it either through the terminal (tar.gz), or by right clicking it and click on unzip in the menu.
* after the unziping, opening Zotero should be as easy as double clicking on the file in the folder simply named `zotero.desktop`

## Shortcut
* to make a zotero shortcut press `Ctrl+Shift` then click and drag the icon for the `zotero.desktop` file to another location, and let go of the left mouse button
* wherever you droped the icon you dragged, a new shortcut for zotero should appear
* note that this shortcut cannot be added to a panel, for that you need a [launcher](https://github.com/P-OEM/P-OEM-s-void-setup/tree/launcher)
    * maybe you could add this shortcut to the `/usr/share/applications` folder to use it as a launcher
