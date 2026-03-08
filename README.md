### [Main branch](https://github.com/P-OEM/P-OEM-s-void-setup)
     
# NFTables
### this branch contains a simple guide for setting up an NFTables firewall in a void linux xfce environment

## [NFTables introduction](#introduction)
## [NFTables instruction](#instruction)

## Introduction
* it is expected that the `nftables` package is installed

* `NFTables` is a tool for setting up your firewall
    * it's the modern succesor to `iptables` (IPv4 usage) and `ip6tables`
        * to put it simply, you need one tool instead of two to secure both IPv4 and IPv6 with `NFTables`

* there is a pretty good guide for setting up `NFTables` in the void linux firewall [Documentation](https://docs.voidlinux.org/config/network/firewalls.html), especially if combined with the `NFTables` wiki example for your type of system

* `NFTables` has a pretty useful wiki [wiki](https://wiki.nftables.org/wiki-nftables/index.php/Main_Page) page
    * by far the most useful part for most people reading this guide will be the [examples](https://wiki.nftables.org/wiki-nftables/index.php/Main_Page#Examples), and more specifically the [Simple ruleset for a workstation](https://wiki.nftables.org/wiki-nftables/index.php/Simple_ruleset_for_a_workstation) example for the person most likely to read this guide

* just like its predecessors, `NFTables` interacts with `netfilter` to filter packages.
    * If you're interested in learning more about linux firewall in general, I highly recommend reading up on the netfilter page [here](https://www.netfilter.org/) 

## Instruction
* start by making a config file for `NFTables`
    ```sh
    sudo touch /etc/nftables.conf
    ```
* then open the `nftables.conf` file as super user (sudo) and add this
    ```sh
    flush ruleset

    table inet filter {
	    chain input {
		    # drop all incomming packages
		    type filter hook input priority 0; policy drop;

            # accept any localhost traffic
            iif lo accept

            # accept traffic originated from us
            ct state established,related accept

		    # accept ssh, http and https ports
		    tcp dport { 22, 443, 80 } accept

		    # allow NTP (Network Time Protocol) port
		    tcp dport { 123 } accept

            # accept neighbour discovery otherwise IPv6 connectivity breaks
            icmpv6 type { nd-neighbor-solicit, nd-router-advert, nd-neighbor-advert } accept
	    }
    }
    ```
    * this is almost the same as [Simple ruleset for a workstation](https://wiki.nftables.org/wiki-nftables/index.php/Simple_ruleset_for_a_workstation) inet example, except I've added a way for NTP to work so your `chrony` [installation and setup](https://github.com/P-OEM/P-OEM-s-void-setup/tree/date-and-time) isn't completely wasted

* then simply make the service available for the system
    * in terminal run
        ```sh
        sudo ln -s /etc/sv/nftables/ /var/service
        ```
    * now you can take the service up or down with:
        ```sh
        sudo sv up nftables
        ```
        ```sh
        sudo sv down nftables
        ```

* then to apply the rules of `nftables.conf` at startup, install the `runit-nftables` package
