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
