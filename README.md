### [Main branch](https://github.com/P-OEM/P-OEM-s-void-setup)

# Docker setup
## this branch contains a simple guide for setting up docker on a void linux system, using glibc and xfce

## [Docker introduction](#introduction)
## [Docker enable containerd and docker service](#enable-containerd-and-docker-service)

## Introduction
* for this guide it's expected that the `docker` package is installed
* docker is a tool that let you run contained vm
    * it's pretty fast, and as far as I understand, it's because it uses the OS engine
* to run docker after this setup, you will have to run it as super user with `sudo`
    * this is void after all, your user can't be allowed to just run things

## Enable containerd and docker service
* to enable these services in void linux, run the following commands in the terminal
```sh
sudo ln -s /etc/sv/containerd /var/service
```
```sh
sudo ln -s /etc/sv/docker /var/service
`````
