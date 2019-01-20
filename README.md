# Mikrotik RB951G-2HnD ethernet fix kernel module

## Goal

The link between AR9344 CPU and AR8327 gigabit ethernet switch (GMAC0) is not working by default under OpenWRT.

It is needed to write some registers to activate communication between the CPU and the gigabit ethernet switch.

This module is intended to properly configure the CPU GMAC0 to fix the communication with the gigabit ethernet switch.

*Note: This module has been tested with OpenWRT 18.03.1.*

## Compilation

*Prerequisite: clone OpenWRT source code*

1. Change OpenWRT source code directory in Makefile.
2. ```make```


## Installation

1. Copy rb951g-2hnd-eth-fix.ko to your router
2. Copy rb951g-2hnd-eth-fix.ko to /lib/modules/<kernel version>
3. ```modprobe rb951g-2hnd-fix-eth```
