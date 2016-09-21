[linux](index.md) | [security](../security/index.md)

## linux security

- [encryption](#encryption)
  - [eCryptfs](#ecryptfs)
  - [GnuPG](#gnupg)
  - [steghide](#steghide)
- [firewalls](#firewalls)
- [rootkits](#rootkits)
  - [rkhunter](#rkhunter)
  - [chrootkit](#chrootkit)

### encryption

#### eCryptfs
- `sudo apt-get install ecryptfs-utils`
- `sudo mount -t ecryptfs /srv /srv`
- [homepage](http://ecryptfs.org/) | [help.ubuntu](https://help.ubuntu.com/lts/serverguide/ecryptfs.html) | [Linux Journal](https://www.linuxjournal.com/article/9400) | [StackExchange](https://stackexchange.com/filters/33360/ecryptfs)
- [How to Encrypt Directories with eCryptfs on Ubuntu 16.04](https://www.howtoforge.com/tutorial/how-to-encrypt-directories-with-ecryptfs-on-ubuntu-16-04/) | [eCryptfs on Ubuntu 9.04](http://bodhizazen.net/Tutorials/Ecryptfs/)

#### GnuPG (GPG)
- `gpg -c filename.txt`: encrypts with a symmetric cipher.. Will prompt to enter a passphrase.
- `gpg filename.txt.gpg`: to decrypt

#### steghide
- `steghide embed -cf /home/user/coverfile.jpg -ef /home/user/top_secret_info.txt -p password12345`: hide top_secret_info.txt inside coverfile.jpg, encrypt with AES
- `steghide extract -sf /home/user/coverfile.jpg`: then enter password to extract.

`ef`: embed file | `cf`: cover file

### firewalls

#### ufw
Ubuntu ships with a tool called `ufw` that can be used to configure your firewall policies
- `sudo ufw allow ssh`: if ssh port has not been changed from default port 22
- `sudo ufw 80/tcp`: exception to run a web server
- `sudo ufw 25/tcp`: exception to allow email on SMTP
- `sudo ufw show added`: show added exceptions
- `sudo ufw enable`
- `sudo ufw status`

### rootkits
'A rootkit is a stealthy type of software, typically malicious, designed to hide the existence of certain processes or programs from normal methods of detection and enable continued privileged access to a computer' -  [Wikipedia](http://en.wikipedia.org/wiki/Rootkit)

#### RkHunter
Use RKHunter & Chkrootkit to detect Rootkits in Linux Mint (Ubuntu).
Installation for rkhunter and chrootkit :

- `sudo apt-get install rkhunter`
- `sudo rkhunter --check` / `sudo rkhunter -c`
- `sudo rkhunter --help`

writes to /var/log/rkhunter.log

#### chkrootkit
- `sudo apt-get install chkrootkit`
- `sudo chkrootkit`
- `sudo chrkrootkit --help`

---

See also [network tools](network.md) | [SSH](network.md#ssh---secure-shell)
