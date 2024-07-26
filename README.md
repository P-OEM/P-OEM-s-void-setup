### [Main branch](https://github.com/gamingtruble/gamingtruble-s-void-setup/tree/main)

# Launcher setup
### this branch contains a simple guide for setting up a launcher for applications in a void linux system with the xfce desktop environment

## [Launcher introduction](#introduction)
## [Launcher GUI setup](#gui-setup)
## [Launcher GUI searchable setup](#gui-searchable-setup)
## [Launcher terminal setup](#terminal-setup)

## Introduction
* this guide expect that there's a folder with a program you would like to make a launcher for in the user home directory
* this guide contains two different ways of setting up a launcher
    * 1. GUI setup
        * can be done almost entirely without any use of the terminal, you might need to run one command to start the file explorer as super user
    * 2. Terminal setup
        * generally the simplest way of setting up a launcher, I would recommend doing this at least once to gain a greater understanding of what's done

## GUI setup
* to make a new launcher, go to desktop, click the right mouse button, and click `create launcher...` (should be the option at the top)
* then add the launcher properties
* the command must path to the program you want to launch, and it starts from `~`/ home folder
    * example
        * Name = My program
        * Comment = launch My program 
        * Command = folder/MyProgram
        * Working Directory = /home/UserName
            * the `UserName` text must be swapped with your users username
    * tip, check to see if the icon pack contains an icon for your program
* then save, and that's it

## GUI searchable setup
* for now, both the shortcut and the launcher is not searchable
* the launcher is a `.desktop` file on your desktop, and the way it is now, it could almost go straight to `/usr/share/applications` directory and work
* to add the missing piece you need to
    * open the launcher file in a text editor (like mousepad)
    * go to the line with `Exec=`
    * remove everything on the path before `folder/MyProgram`
* now the file is ready to be placed in the `/usr/share/applications` folder (directory)
    * steps to do this:
        * start your file manager with root access
            * in the terminal `sudo file-managers-name`
        * then go to the top folder/ root directory
        * then go to `/usr/share/applications`
        * then cut or copy and paste the launcher application from desktop into `/usr/share/applications`
        * then log the user out and back in again
        * then try to search and start the application (alt+f2 or f3 by default)
    * for this to work, it's crucial that the `Working Directory = /home/UserName` (this is `Path=/home/UserName` when opening with text editor) part is set correctly

## Terminal setup
* start by picking your favourite terminal text edditing program (examples: vi, vim, nvim or nano) or decide on how you want to pipe the information directly to the file
* then use sudo to add a `.desktop` file (example `MyApplication.desktop`) to `/usr/share/applications`
    * examples
        * text editor
            * run `sudo vi /usr/share/applications/MyApplication.desktop` in the terminal
            * then add this to the file
                ```cmd
				# comments start with "#"
				[Desktop Entry]
				Type=application
				Name=My application
				Comment=My application launcher
				Exec=folder/MyApplication
				Icon=insertIconPath
				Path=/home/UserName
				Categories=Game (can be something else like "Office")
				```
        * piping
            * `su`
                * `printf "[Desktop Entry]\nType=application\nName=My application\nComment=My application launcher\nExec=folder/MyApplication\nIcon=InsertIconPath\nPath=/home/UserName\nCategories=Game (can be something else like "Office")" > /usr/share/applications/MyApplication.desktop`

* in both the examples:
    * make sure `Path` lead to the user home directory, and the `Exec` path from there to the application, make sure that this is the way you set it up
    * make sure you swap out generic or extra information
* here's two links with a little extra on `.desktop` files
    * simple: [How to Create a Desktop Launchers in Linux](https://www.tecmint.com/create-linux-desktop-launchers/)
    * advanced: [Desktop Entry Specification](https://specifications.freedesktop.org/desktop-entry-spec/desktop-entry-spec-latest.html)
