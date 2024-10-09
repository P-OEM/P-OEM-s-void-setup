### [Main branch](https://github.com/P-OEM/P-OEM-s-void-setup/tree/main)

# Thunderbird setup
### this branch contains a simple guide for setting up thunderbird in a xfce, void linux system, with my preferences

## [Thunderbird introduction](#introduction)
## [Thunderbird importing filters](#importing-filters)
## [Thunderbird basic look](#basic-look)

## Introduction
* it is expected that the thunderbird package is installed before using this guide
* for this guide, you will not need the terminal
* setting up thunderbird is pretty straight forward
    * just make sure you installed the package, and log on with your favorite email
        * curse the microsoft email account compatability, and you're ready to go
* the one thing that can be a bit tricky is folders and filters
    * it's ok ish setting them up, but moving your setup can be a bit tricky
* I'm not going to explain setup, [here's](https://support.mozilla.org/no/kb/organize-your-messages-using-filters) a guide for that

## Importing filters
* to import already existing filters to your installation, you need to locate the email folder where you want the filters to be applied, and add the file for your filters
* open your file manager, and navigate to your users home folder
    * then hit `ctrl` + `h` to unhide all `.` files (`MailVersion` = `Imap` or `Pop`)
        * then click on `.thunderbird`, and go to `.thunderbird/oneOfTheRandomSymbolsFolders.default/MailVersionMail/MailVersion.yourEMailsDomain.topDomain/`
            * then add or replace `msgFilterRules.dat` in that folder
                * you can use the same pathing for finding the file, by going to the same folder on the system you want the filters from
                    * as far as I know, there's no official way to syncronise your filters
                        * my answer to this critical issue, is leaving my filter file in a dropbox folder, and making a shortcut for it to the thunderbird folder 𓅪
                            * you can of course make something working with github, by using a `.sh` file to launch thunderbird and do a pull, then push command whenever it launches, but personally I'll stick to my KISS solution for this
## Basic look
* burger menu up to the right
    * view
        * layout
            * classic view
        * Toolbars
            * Quick Filter Bar
* message list display options (under the `X` symbol for closing window)
    * table view
* after that
    * go to date
        * click so arrow stand `^`
