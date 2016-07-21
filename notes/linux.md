[notes](notes.md)

## Linux

**[terminal](linuxTerminal.md)**

### Filesystem
`/etc`: Stores config files for the system.

`/var/log`: Stores log files for various system programs. (You may not have permission to look at everything in this directory. Don't let that stop you exploring though. A few error messages never hurt anyone.)

`/bin`: The location of several commonly used programs (some of which we will learn about in the rest of this tutorial.

`/usr/bin`: Another location for programs on the system

`r-alt` set as compose key (special characters)
Ctrl + m minimize


PPA - Personal Package Archives

APT - Advanced Package Tool


### Applications
- Privacy Badger ( browser addon )
- k4dirstat
- deborphan, gtkorphan
- preload: make faster, adaptive readahead daemon


gksu gedit /etc/sysctl.conf              (change swappiness)

gksu gedit, in preferences, disable file browser plugin

### Booting
- MBR
- GRUB: GRand Unified Boot Loader
- POST: power on self test
- BIOS (EFI, UEFI)

#### Master Boot Record (MBR)
located in 1st sector of primary disk, usually /dev/hda or /dev/sda.
less than 512 bytes

3 parts
- boot loader
- partition table info
- magic numbers???

loads & executes GRUB
loads default kernel specified in config file /etc/grub.conf
