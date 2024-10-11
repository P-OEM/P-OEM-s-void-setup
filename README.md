### [Main branch](https://github.com/P-OEM/P-OEM-s-void-setup)

# General solutions
### this branch contains simple solutions to issues on a void linux system with the xfce desktop environment

## [General solutions introduction](#introduction)
## [General solutions structure](#structure)
## [General solutions issues link section](#issues)
## [General solutions solutions link section](#solutions)

## Introduction
* the branch contains two sets of extra lists for links
    * issues and solutions
        * issues is where you would go to look for similar issues to what you've encountered
            * the links in issues start with the name of the tool containing the issue, followed by a short description of the issue
            * the tool title may not be the same as the title in the document, but it's most likely the title of a tool that fall under the tool in the actual title
        * solutions is where you would go to look for solutions belonging to a tool
            * the links in solutions contains the tool titles

* all of the issues and solutions links are local
* the issues and solutions on this branch are categorized alphabetically
* multiple issues can have the same solution

## Structure
* there's a simple structure to the solutions on this branch:

* `Title`
    * `solution (this can be multiple dots)`
        * `source (this link might be available, as a source for the solution)`

## Issues
<details>

### [Terminal: left something sensitive in the log](#clear-bash-cache)
### [Thunderbird: keeps closing when I try to look at email](#move-folder-to-gain-space)
### [Workspace: not starting into the first workspace](#clear-session-cache)
</details>

## Solutions
<details>

### [Solutions terminal](#terminal)
### [Solutions thunderbird](#thunderbird)
### [Solutions xfwm4](#xfwm4)
</details>

## terminal
### clear bash cache
* in your home directory run
    * `rm .bash_history`

## thunderbird
### move folder to gain space
* in you home directory, find `.thunderbird`
    * move the directory to another directory and back
        * source? trust me bro XD
            * I forget exactly how folder (directory) space work in linux, but I think linux determine this whenever you make one or download something
                * this fix should simply make linux reconsider the amount of space your thunderbird directory needs, by manualy moving it so that the system must do the calculation again

## xfwm4
### clear session cache
* this will remove the cached information from earlier login sessions
    * in your home directory run
        * `rm -rf .cache/sessions/*`
            * [source](https://docs.xfce.org/xfce/xfwm4/faq)
