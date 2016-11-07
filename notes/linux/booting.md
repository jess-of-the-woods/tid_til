[linux](index.md)

## Booting
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


### Runlevels
Analogous to recovery mode in windows.

1. Single-user
2. Reserved on most systems (full GUI with multi-user on Debian)
3. Full multi-user with no GUI
4. Undefined
5. Full multi-user with GUI
6. Reboot


---

 See also [filesystem](filesystem.md)
