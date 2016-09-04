[linux](index.md)

## Security

'A rootkit is a stealthy type of software, typically malicious, designed to hide the existence of certain processes or programs from normal methods of detection and enable continued privileged access to a computer' -  [Wikipedia](http://en.wikipedia.org/wiki/Rootkit)

### RkHunter
Use RKHunter & Chkrootkit to detect Rootkits in Linux Mint (Ubuntu).
Installation for rkhunter and chrootkit :

- `sudo apt-get install rkhunter`
- `sudo rkhunter --check` / `sudo rkhunter -c`
- `sudo rkhunter --help`

writes to /var/log/rkhunter.log

### chkrootkit

- `sudo apt-get install chkrootkit`
- `sudo chkrootkit`
- `sudo chrkrootkit --help`
