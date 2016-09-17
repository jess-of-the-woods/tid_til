[linux](index.md) | [security](../security/index.md)

## linux security

### encryption

#### GnuPG (GPG)
- `gpg -c filename.txt`: encrypts with a symmetric cipher.. Will prompt to enter a passphrase.
- `gpg filename.txt.gpg`: to decrypt

#### steghide
`steghide embed -cf /home/user/coverfile.jpg -ef /home/user/top_secret_info.txt -p password12345`: hide top_secret_info.txt inside coverfile.jpg, encrypt with AES

`steghide extract -sf /home/user/coverfile.jpg`: then enter password to extract.

- ef: embed file
- cf: cover file

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

See also [network tools](network.md)
