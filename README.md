### [Main branch](https://github.com/gamingtruble/gamingtruble-s-void-setup)

# Git setup
## this branch contains a simple guide for setting up git on a void linux system, using glibc and xfce

## [Git introduction](#introduction)
## [Git global config setup](#global-config-setup)

## Introduction
* for this guide it's expected that the `git` package is installed
* git is a version controll tool
    * the tool can help you keep track of file versions
    * the tool can be connected and store versions on Github (duh)

* for now this guide only covers how to deal with local credentials

## global-config-setup
* `git config --global user.name "your username"`
* `git config --global user.email youremail@email.com`
* this will delete the password after some time
    * time is in seconds, this is one day
* `git config --global credential.helper 'cache --timeout=86400'`
    * if you don't care about the timeout, you can do `store` instead of `'cache --timeout=86400'`
        * and it seems that it's stored as plaintext localy for as long as you let it... yeah I stick to timeout
