[notes](../index.md)

## Linux

### - [booting](booting.md)
### - [security](security.md)
### - [SSD configuration](SSD.md)
### - [terminal](terminal.md)

---

PPA - Personal Package Archives

### Filesystem

also check out `man hier`: manual pages for filesystem hierarchy


`/`: Represents the root directory

`/bin`: Binary (executable) programs & commands available to the user. The location of many commonly used programs. Also some links to applications installed elsewhere. (`ls -alh /bin | less`). Many GNU utilities.

`/boot`: Boot & system files inc. kernel

`/dev`: Device files & drivers. Lists all hard drives. `ls /dev | grep sd`
- `sd` means regular hard disk, 'sda' would be the 1st disk the system sees, 'sdb' would be the 2nd one.. 'sda1' would be the 1st partition, 'sda2' the 2nd partition

`/etc`: Stores config files for your applications (host-specific). When you install an application it will create a folder with config files in. Also config for user-facing system tools is here.. Cron etc

`/home`: Stores files belonging to each user. In a subdirectory of `/home` e.g. `/home/margaret`

`/lib`: shared libraries, kernel modules. Used by many programs on the system.

`/media`: mount point for removable media (specific to Ubuntu). Where things get automounted

`/mnt`: Mount point for temporary file systems

`/opt`: Optional. Programs installed by user

`/proc`: Where the kernel writes information about running processes. A virtual filesystem where the kernel is able to communicate with the user & any other program on the machine about the state of processes that are running. There will be a directory in /proc for each running process.

`/root`: root's home

`/sbin`: System binaries

`/tmp`: Temporary files, destroyed on restart.

`/usr`: unix system resources

`/usr/bin`: Another location for programs on the system

`/var`: Variables. Variable data which changes over time. e.g. mail spools, user databases, log files

`/var/log`: Stores log files for various system programs.
