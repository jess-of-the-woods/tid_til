[linux](index.md) | [terminal](terminal.md)

## storage devices

#### - [SSD configuration](SSD.md)
- [device file naming](#device-file-naming)
- [mount/umount](#mount)
- [fdisk](#fdisk)
- [mkfs](#mkfs)
- [fsck](#fsck)
- [disk usage](#disk-usage)

storage devices are typically mounted at `/mnt` or `/media`

### device file naming
#### SCSI devices
- /dev/sdx
`sd` means regular hard disk, 'sda' would be the 1st disk the system sees

'sdb' would be the 2nd one.. any partitions are indicated by numbers e.g. 'sda1': 1st partition, 'sda2': 2nd partition

####USB & SATA
follow SCSI convention

#### PATA devices
- /dev/hdx (rarely used nowadays)

### mount
- `mount`: to display mounted devices
- `sudo mount /dev/sdb /mnt/flash`: to mount 'sdb' device at `/mnt/flash`
- `sudo mount -U <UUID> /mnt/flash`
- `sudo umount /mnt/flash`: to unmount

### fdisk
manipulate disk partition table
- `sudo fdisk -l` or `sudo fdisk -l | grep sda`: list all partitions

### mkfs
build a linux filesystem. mkfs is just a frontend to a bunch of scripts with names like mkfs.ext2
- `mkfs -t ext3 /dev/hdx`: formatting a disk
linux only supports read-only for NTFS filesystems

### fsck
check & repair a linux filesystem. runs only on unmounted filesystems.
- `fsck /dev/sda1`

### disk usage
- `lsblk`: list info about block devices
- `baobab`: open disk usage analyser

#### df
report file system disk space usage. e.g. `df -ah`

**switches**:
- `-a`: all
- `-h`: human-readable

---

See also [du](terminal.md#du) | [filesystem](filesystem.md) (esp. `/dev`) | [SSD config](SSD.md)
