[linux](index.md) | [terminal](terminal.md)

## file types

### - [file permissions](file_permissions.md)

first file attribute bit that's displayed when you type "ls -l"

- files. a series of bits. has a `-` for first bit of permission string
- directories - references to files (similiar to a link). has a `d` for first bit
- symlinks - has an `l` for first bit

### Interface files for your hardware
- character device files, e.g. mice. where the mouse writes information about where it is moving. the system then takes & uses that info. character devices take care of their own buffering. has a `c` for first bit
- block device files e.g. hard drives. buffer on the kernel (kernel provides buffering). has a `b` for first bit



<!-- ---

See also -->
