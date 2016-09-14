[linux](index.md) | [hardware](../hardware.md)

## Linux config for SSD's

garbage collection: `sudo fstrim -v /`

also add `fstrim /` to `/etc/rc.local`

<!-- ### Mount files on boot
config file for mounting: `etc/fstab`
 -->
### If you have server running 24/7..
in `/etc/cron.daily` create a file `ssd_trim`. inside file type the following:

```bash
fstrim /
exit 0
```

then `chmod +x ssd_trim`

### Swappiness

disable swappiness: `sudo nano /etc/sysctl.conf`

will take effect after reboot


<!-- ---

See also -->
