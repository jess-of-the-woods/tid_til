[linux](index.md)

## storage devices

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

### fdisk
manipulate disk partition table
- `sudo fdisk -l` or `sudo fdisk -l | grep sda`: list all partitions

See also [filesystem](filesystem.md) (esp. `/dev`)
