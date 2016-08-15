[notes](notes.md)

## Linux

**[terminal](linuxTerminal.md)**

### Filesystem Locations

`/`: Represents the root directory

`/bin`: Binary (executable) programs & commands available to the user. The location of several commonly used programs

`/etc`: Stores config files for the system.

`/opt`: Optional. Programs installed by user

`/home`: Stores files belonging to each user. In a subdirectory of `/home` e.g. `/home/margaret`

`/mnt`: Where new devices such as USB drives will be mounted

`/var`: Variables. Variable data which changes over time. e.g. mail spools, user databases, log files

`/tmp`: Temporary files

`/var/log`: Stores log files for various system programs.

`/usr`: unix system resources

`/usr/bin`: Another location for programs on the system

### Other
- Ctrl + m minimize

### GKSu
GKSu is a library that provides a Gtk+ frontend to su and sudo. It supports login shells and preserving environment when acting as a su frontend. It is useful to menu items or other graphical programs that need to ask a user's password to run another program as another user.

gksu gedit /etc/sysctl.conf     (change swappiness)

gksu gedit, in preferences, disable file browser plugin

PPA - Personal Package Archives

APT - Advanced Package Tool

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
