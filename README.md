### [Main branch](https://github.com/P-OEM/P-OEM-s-void-setup)

# Powerline-go setup
### this branch contains a simple guide for setting powerline-go in a void linux xfce environment using bash

## [Powerline-go introduction](#introduction)
## [Powerline-go setup instruction](#instruction)

## Introduction
* for this guide it is expected that the `go` and `powerline-go` packages are installed
* this guide will show how to install and use `powerline-go`

## Instruction
* with the packages installed, open or make the `.bashrc` in your home folder
    * then paste whatever is [here](https://github.com/justjanne/powerline-go?tab=readme-ov-file#bash) after the text in the file
        * optionally, paste this for newlines in the text (this may be outdated tho):
        ```sh
        # powerline go lang version
        function _update_ps1() {
        PS1="$(powerline-go \
            -error $? \
            -jobs $(jobs -p | wc -l) \
            -cwd-max-depth 1 \
            -condensed \
        )"
        }

        if [ "$TERM" != "linux" ] && [ -f "$GOPATH/bin/powerline-go" ]; then
            PROMPT_COMMAND="_update_ps1; $PROMPT_COMMAND"
        fi
        ```
* then restart terminal
