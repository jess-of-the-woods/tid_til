[linux](index.md) | [terminal](terminal.md)

## cron

task scheduler

each user has a crontab (cron table), which is their table of scheduled tasks they want to be completed at some point in the future.

- `crontab -l`: to list
- `crontab -e`: to edit

`/var/spool/cron/crontabs`: user crontabs are kept here. not advisable to edit through here.

if you need to edit a specific users crontabs, `sudo -i`: to become root, then `crontab -e -u username`

`/etc/cron.d`: package-specific crontabs

`/etc/crontab`: system-wide crontab


---

See also
