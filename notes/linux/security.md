[linux](index.md) | [security](../security/index.md) | [terminal](terminal.md)

## linux security

- [sudo/su](#sudo--su)
  - [GKSu](#gksu)
- [encryption](#encryption)
  - [eCryptfs](#ecryptfs)
  - [GnuPG](#gnupg)
  - [steghide](#steghide)
- [firewalls](#firewalls)
- [rootkits](#rootkits)
  - [rkhunter](#rkhunter)
  - [chrootkit](#chrootkit)
- [hashing algorithms](#hashing-algorithms)
- [user account management](userMgmt.md)

### sudo / su
`su`: superuser. Typing `su` followed by root account password (if it has been set up), will log in as superuser/root user. To exit type `exit`.

`sudo` will just allow you superuser access for a single command.. e.g. `sudo apt-get install wine`. This is safer. The OS will remember your password for 15 minutes. If you haven't set up root account & password, you can log in as superuser with `sudo su` using just your user password.

- `sudo -k`: wipe cache

#### GKSu
GKSu is a library that provides a Gtk+ frontend to su and sudo. It supports login shells and preserving environment when acting as a su frontend. It is useful to menu items or other graphical programs that need to ask a user's password to run another program as another user.

- `gksu gedit /etc/sysctl.conf`     (change swappiness)
- `gksu gedit`, in preferences, disable file browser plugin

### /etc/passwd
edit using visudo. has list of all users on system. in following format:

```bash
user-name:x:user-number:group-number:comment section:/home-directory:default-shell
```

for example:
```bash
user1:x:500:500:Greg:/home/user1:/bin/bash
```

### /etc/shadow

### /etc/sudoers
often includes a line like:
```bash
includedir /etc/sudoers.d
```
which will include files in the specified directory

- [sudoers](https://help.ubuntu.com/community/Sudoers)

#### add a user into sudoers
copy file of current user who is in 'sudoers.d' like:
```bash
sudo cp /etc/sudoers.d/vagrant /etc/sudoers.d/newUsersName
```
then edit & change user name in file

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

### hashing algorithms
- MD5
- SHA256

---

See also [network tools](network.md) | [SSH](network.md#ssh---secure-shell)
