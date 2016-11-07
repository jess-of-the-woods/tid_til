[linux](index.md)

## Booting
BIOS (loads & executes MBR boot loader)
- POST: power on self test
- BIOS (EFI, UEFI)

### Master Boot Record (MBR)
Located in 1st sector of primary disk, usually /dev/hda or /dev/sda. Less than 512 bytes

3 parts
- primary boot loader (446 bytes)
- partition table info (64 bytes)
- magic numbers (2 bytes)

loads & executes GRUB

#### GRUB - GRand Unified Boot Loader
multi-boot boot loader which displays a splash screen, waits for a few seconds, if no user input it loads default kernel image specified in config file `/etc/grub.conf`

### Kernel
GRUB gives control to kernel. Kernel resides in RAM until shutdown. First thing kernel will do is start running init (initialisation) process.

Startup scripts are found in /etc/rc.d & similarly named directories. Scripts starting with 'S' will start a service, while those starting with a 'K' will kill a service. The number after the initial letter will show the order in which these scripts are run. The run level will determine which `/etc/rc<number>.d` directory is used, and therefore which scripts will run & which services will initialise

Upstart (Ubuntu) puts these scripts in `/etc/init.d` & upstart specific scripts are in `/etc/init`

### Runlevels
Analogous to recovery mode in windows.

0. Halt
1. Single-user
2. Reserved on most systems (full GUI with multi-user on Debian)
3. Full multi-user with no GUI
4. Undefined
5. Full multi-user with GUI (X11)
6. Reboot

`init <number>`: to change the run level
`runlevel`: to see the current run level

To permanently alter the run level your system boots into, edit `/etc/inittab` on redhat systems, `/etc/init/rc-sysinit.conf` on Ubuntu systems.



---

 See also [filesystem](filesystem.md)
