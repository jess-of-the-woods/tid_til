[notes](../notes.md)

## Linux

### - [booting](booting.md)
### - [security](security.md)
### - [terminal](terminal.md)

---

PPA - Personal Package Archives

APT - Advanced Package Tool

### Filesystem Locations

`/`: Represents the root directory

`/bin`: Binary (executable) programs & commands available to the user. The location of several commonly used programs

`/boot`: Boot & system files inc. kernel

`/dev`: Device files & drivers

`/etc`: Stores config files for the system (host-specific).

`/home`: Stores files belonging to each user. In a subdirectory of `/home` e.g. `/home/margaret`

`/lib`: shared libraries, kernel modules

`/media`: mount point for removable media

`/mnt`: Mount point for temporary file systems

`/opt`: Optional. Programs installed by user

`/sbin`: System binaries

`/tmp`: Temporary files

`/usr`: unix system resources

`/usr/bin`: Another location for programs on the system

`/var`: Variables. Variable data which changes over time. e.g. mail spools, user databases, log files

`/var/log`: Stores log files for various system programs.


### GKSu
GKSu is a library that provides a Gtk+ frontend to su and sudo. It supports login shells and preserving environment when acting as a su frontend. It is useful to menu items or other graphical programs that need to ask a user's password to run another program as another user.

- `gksu gedit /etc/sysctl.conf`     (change swappiness)
- `gksu gedit`, in preferences, disable file browser plugin
