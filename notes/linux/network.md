[linux terminal](terminal.md) | [networks](../networks/index.md) | [tools](../tools.md)

### network tools
- **[rsync](#rsync)**
- **[SSH](#ssh---secure-shell)**
- **[SCP](#scp)**
- **[SSH](../security/SSH.md)**

### commands
- `ifconfig`: configure a network interface, also `ifconfig eth0` [(x)](http://net-tools.sourceforge.net/man/ifconfig.8.html)
- `iwconfig`: wireless information (configure a wireless network interface), check the settings of your wireless connection without editing anything. This also shows packets sent/received.
- `ip addr show`: display network info, similar to ifconfig
- `ping 8.8.8.8`: time to return answer
- `whois`: gets info on domain names or IP's
- `route -n`: see your default gateway
- `traceroute`: shows path to the destination IP (also mtr & tracepath)
- `dig`: domain info groper, translates domains to IP addresses
- `iftop`: displays a table of bandwidth usage by hosts
- `nm-tool`: Network Manager Tool (Network Information)
- `lspci | grep Net`: info about Network Cards (wired & wireless)
- `lsusb`: info about USB devices connected etc.
- `wget`: web get, download a file from an address like: `wget locationToFile`
- `netstat -tulpn`: check for open ports. run as root with `sudo netstat -tulpn` for process id's & program names. `t`: TCP, `u`: UDP, `p`: programs attached to those ports, `l`: listening ports, `n`: listed numerically


### rsync
file copying tool (remote & local)

syntax:

`rsync from to`

e.g.

`rsync -av . root@domain.com:~/mango`: copy all of the files in this directory (`.`) to the /home/bananaUser/mango directory (through SSH 'user@domain')

`rsync --progress --delete -ah source destination`: non-SSH usage

**switches**:
- `a`: archive, preserve file structure etc.
- `h`: human-readable
- `v`: verbose
- `--progress`: show progress
- `--delete`: delete files in destination to keep dir's sync'd

delete a file and run rsync again, and it only copies the one missing file

### SCP - Secure Copy
Syntax:

`scp from to`

e.g. `scp -R user@domain.com:/home/user/Documents/newfiles ~/Desktop`

- `-R`: recursive (grab a whole directory including subfolders)
- `-P`: specify port number e.g. `-P1234`

---

See also [security](security.md)
