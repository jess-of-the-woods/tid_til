[backend](backend.md) | [linux](linux.md) | [tools](tools.md)

## Nix Terminal
- **[Git / Github](git-github.md)**
- [terminal window shortcuts](#terminal-window-shortcuts)
- [basic commands](#basic-commands)
- [system](#system)
- [ls](#ls)
- [cd](#cd)
- [rm](#rm)
- [ln](#ln)
- [grep](#grep), [sed](#sed)
- [chmod](#chmod), [chown](#chown)
- [disk usage](#disk-usage)
- [sudo & su](#sudo-su)
- [managing applications](#installing-/-uninstalling-/-updating-/-managing-/-applications)
- [rsync](#rsync)
- [piping](#piping)
- [redirection](#redirection)
- [BASH scripts](#bash-scripts)
- [network tools](#network-tools)
- [SSH](#ssh)

### terminal keyboard shortcuts
- `ctrl alt t`: open terminal window
- `ctrl shift t`: open new tab
- `ctrl shift n`: open new window
- `ctrl shift w`: close tab
- `ctrl shift q`: close terminal window
- `ctrl pageup` ( `ctrl + fn + up` ): next tab
- `ctrl l`: clear terminal
- `ctrl + r`: reverse search. ctrl + r, then start typing a command you have used recently & it will come up, then press enter. preferable to having to retype long commands again & again.
- `ctrl a`: start of line
- `ctrl e`: end of line
- `ctrl p`: previous command
- `ctrl n`: next



### basic commands
`pwd`: Print Working Directory

`clear`: clear screen (also ctrl + l)

`mv`: move file(s), source file(s) then destination

`cp`: copy file(s), source file(s) then destination

`touch`: creates empty file, `touch stuff.txt`

`wc`: 'Word Count' lines, words, characters, eg. `cat filename | wc`

`mkdir`: creates directory, `mkdir dirname`

`cat`: outputs contents of file to terminal, `cat filename`

`sort`: Orders Alphabetically, `sort filename.*` or `cat lakes.txt | sort > sorted_lakes.txt`

`uniq`: filters out adjacent duplicate lines & outputs contents, `uniq filename`

`file /user/home/filename.txt`: tells you document type

`less`: Output file contents to screen, e.g. `less filename`. see also 'more'

`more`: prints out file to screen, page by page

`head`: first 10 lines of a file, e.g. `head filename`

`tail`: last 10 lines of a file. also `tail -f filename`: follows a file.. (as it changes over time)

`nano path/filename`: Open file in Nano editor ( ctrl + O to save, ctrl + X to exit )

`history`: Displays recent commands

`history -c`: Clears history (stored in ~/.bash_history)

`alias | wc -l`: Number of Aliases

`find ~/Downloads theFileImLookingFor`: Finds files/directories.


### System
- 'man': manual pages. Use like: `man ls` or `man uniq` for manual pages on the ls or uniq commands
- help. to get help on a command type like: `ls --help`
- `$`: represents prompt in BASH?
- `.`: represents current directory
- `..`: represents parent directory, `cd ..`: change to parent directory
- ` ~`: (tilde) represents users home directory eg. `/home/user`, can use in relative paths e.g. `~/Documents/` is the same as `/home/user/Documents`
- `~/.bash_profile`: used to store environment settings for terminal (source ~/.bash_profile activates changes))
- 'alias' is another name for keyboard shortcut in the terminal, defined in .bashrc or .zshrc etc as

`alias tek="cd ~Documents/tech"`



`shutdown` `shutdown -h`: halt/turn off. `shutdown -r +30`: restart in 30 minutes, `shutdown -h now`: turn off now

also `poweroff` or `init 0` do the same

`init 6`: reboot


#### 'System' Commands:
- `tty`: displays the virtual terminal you are using..
- `whoami`: displays username
- `who am i`: displays username & terminal you are in.
- `hostname`: displays hostname (name of computer)
- `uname`: print system information. `uname -a` prints all
- `service udev status`: Check if 'udev' service is running (on older machines)
- `systemctl status udev`: Check if 'udev' service is running (on newer machines)
- `ps aux | grep nginx`: check CPU usage for a process (nginx)
- `top`: check CPU usage for a processes


### ls
- `ls` - list files (`-l` long form, `-a` hidden files & directories, `-t` sort by time modified)
- `ls /bin`: list files/folders in /bin

### cd
- `cd ../..`: change directory
- `cd /` goes to root (as does `/`)
- `cd` goes to home

### rm
- `rm` ( remove files & directories, -r recursive )
- `rm -rf dirname`: removes non-empty dir ( recursive & force )

### ln
creates links to files or folders
- `ln file1 yea`: creates hard link to file1. link is called yea
- `ln -s file1 yea`: creates symlink (soft) to file1. If file1 is deleted, link will not work..
- [more info](http://www.unixtutorial.org/commands/ln/)

### grep
- 'G'lobal 'Re'gular expression 'P'rint (regex)
- used to look for line that matches a pattern in files
- `grep "foo" words.txt` or `grep -i "foo" words.txt` or `grep -R searchterm /home/user/`
- `-i`: case-insensitive
- `-R`: recursive
- `-v`: invert
- `-n`: line number
- `^`: start of line
- `$`: end of line
- `..cept` finds `accept`, `except`

### sed
'stream editor', accepts standard input and modifies it based on an expression, before displaying it as output, for filtering & transforming text


### chmod
'change mode' change the access permissions to file system objects (files and directories).
- `chmod`: change mode, modify permission string
- `chmod +x`: adds execution rights
- `chmod -x`: removes execution rights

`chmod 644 filename` or `chmod 777 filename`

### chown
'change owner' or group of object
- `chown -R ghost:ghost .` chown recursively, group: ghost, user:ghost, `.` is current dir

### Disk Usage
- `df -ah` `-a`: all, `-h`: human-readable
- `du -hs ./path/to/dir` ( du = disk usage, h = human-readable, s = summary ) recursive summary of folder & subfolders..
- `lsblk`: list info about block devices
- `baobab`: open disk usage analyser

### sudo / su
`su`: superuser. Typing `su` followed by root account password (if it has been set up), will log in as superuser/root user. To exit type `exit`.

`sudo` will just allow you superuser access for a single command.. e.g. `sudo apt-get install wine`. This is safer. The OS will remember your password for 15 minutes. If you haven't set up root account & password, you can log in as superuser with `sudo su` using just your user password.

### installing / uninstalling / updating / managing applications

`sudo apt-get install packagename`: Install a package/program

`sudo apt-get remove packagename`: Remove a package/program

`sudo apt-get update`: Update repo's

`sudo add-apt-repository ppa:numix/ppa`: Add repository

`sudo apt-get autoremove`: Remove dependencies for programs which are no longer installed

`ls /usr/share/applications | awk -F '.desktop' ' { print $1}' - > ~/Desktop/applications.txt`: List of installed applications

### rsync

copy all of the files in this directory (`.`) to the /home/bananaUser/mango directory (through SSH 'user@domain')

e.g. `rsync -av . root@domain.com:~/mango`

non SSH usage: `rsync --progress --delete -ah source destination`

switches:
- `a`: archive, preserve file structure etc.
- `h`: human-readable
- `v`: verbose
- `--progress`: show progress
- `--delete`: delete files in destination to keep dir's sync'd

delete a file and run rsync again, and it only copies the one missing file

### piping
`|` (pipe) pipes output of one command to another (see basic commands)

Syntax:

`sort deserts.txt | uniq > uniq-deserts.txt`

sort deserts.txt, pipe to `uniq`, redirect to newfile.

### redirection
redirect output to file
`>`

Syntax:

`cat filename > otherFilename`

### BASH scripts
starts with hashbang (`#!`) & reference to thing that runs the script e.g.
- `#! /bin/bash`: bash script
- `#! /usr/bin/env node`: node script

- [Beginners Bash Scripting](https://help.ubuntu.com/community/Beginners/BashScripting)

### network tools
- `ifconfig`: configure a network interface [(x)](http://net-tools.sourceforge.net/man/ifconfig.8.html)
- `ip addr show`: display network info, similar to ifconfig
- `ping 8.8.8.8`: time to return answer
- `whois`: gets info on domain names or IP's
- `traceroute`: shows path to the destination IP
- `dig`: domain info groper, translates domains to IP addresses
- `iftop`: displays a table of bandwidth usage by hosts
- `nm-tool`: Network Manager Tool (Network Information)
- `lspci | grep Net`: info about Network Cards (wired & wireless)
- `lsusb`: info about USB devices connected etc.
- `wget`: web get, download a file from an address like: `wget locationToFile`
- `netstat -tulpn`: check for open ports. run as root with `sudo netstat -tulpn` for process id's & program names

#### SSH - Secure Shell

syntax:

ssh [user]@[ip address] / [domain]

e.g.

`ssh user@192.x.x.x` or `ssh user@mydomain.com`

`exit`: to logout

##### SSH Keys
`ssh-keygen -t rsa`: to generate keys. '-t' for type

can either use a passphrase or not

`ssh -C 'email@email.com'`: '-C' is a comment

`find / -name sshd_config`

- [How SSH Works](https://www.youtube.com/watch?v=zlv9dI-9g1U)
- [Setting up SSH Keys](https://www.youtube.com/watch?v=-J9wUW5NhOQ) - YouTube

### tmux (terminal multiplexer)
- `tmux`  to enter tmux
- `ctrl + b` then `?` for help (list commands)
- `exit`: to exit
