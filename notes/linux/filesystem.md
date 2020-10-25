[linux](index.md) | [terminal](terminal.md)

## linux filesystem

- **[file storage](#file-storage)**
- **[filesystem hierarchy](#filesystem-hierarchy)**

### file storage
- [file types](filetypes.md)
- [file permissions](file_permissions.md)

#### inodes
An inode (information node) is a set of details about a single file on a disk, including:
- file size
- creation, access & modification times
- owner & group
- permissions
- file type
- link count
- starting block number

An inode number is a reference to an inode in the inode table.
- `ls -i`: to display inode numbers for files

An inode table is a table with the information listed above connected to inode numbers (which each represent a single file)

### filesystem hierarchy
also check out `man hier`: manual pages for filesystem hierarchy

`/`: Represents the root directory

`/bin`: Binary (executable) programs & commands available to the user. The location of many commonly used programs. Also some links to applications installed elsewhere. (`ls -alh /bin | less`). Many GNU utilities.

`/boot`: Boot & system files inc. kernel

`/dev`: Virtual filesystem created at runtime by the kernel with all device files & drivers. (lists all hard drives.) `ls /dev | grep sd`. (cf. [storage devices](storage_devices.md))

`/etc`: Stores config files for your applications (host-specific). When you install an application it will create a folder with config files in. Also config for user-facing system tools is here.. Cron etc

`/home`: Stores files belonging to each user. In a subdirectory of `/home` e.g. `/home/margaret`

`/lib`: shared libraries, kernel modules. Used by many programs on the system.

`/media`: mount point for removable media (specific to Ubuntu). Where things get automounted

`/mnt`: Mount point for temporary file systems

`/opt`: Optional. Programs installed by user

`/proc`: Where the kernel writes information about running processes. [more info](processes.md#proc-filesystem)

`/root`: root's home

`/sbin`: System binaries

`/tmp`: Temporary files, destroyed on restart.

`/usr`: unix system resources

`/usr/bin`: Another location for programs on the system

`/var`: Variables. Variable data which changes over time. e.g. mail spools, user databases, log files

`/var/log`: Stores log files for various system programs.



---

see also [booting](booting.md) | [storage devices](storageDevices.md)
