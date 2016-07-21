[notes](notes.md) | [backend](backend.md) | [tools](tools.md)

## Nix Terminal
- **[Git / Github](git-github.md)**
- [Terminal Window Keyboard Shortcuts](#terminal-window-shortcuts)
- [shell scripts](#shell-scripts)
- [basic commands](#basic-commands)
- [ls](#ls)
- [cd](#cd)
- [rm](#rm)
- [ln](#ln)
- [grep](#grep)
- [sed](#sed)
- [chmod](#chmod)
- [chown](#chown)
- [disk usage](#disk-usage)
- [Installing / Uninstalling / Updating / Managing applications](#installing-/-updating)
- [piping / redirection](#piping-redirection)
- [Network Tools](#network-tools)
- [other](#other)

### Terminal window shortcuts
- `ctrl alt t`: Open terminal window
- `ctrl shift t`: Open new tab
- `ctrl shift n`: Open new window
- `ctrl shift w`: Close tab
- `ctrl shift q`: Close terminal window
- `ctrl pageup` ( `ctrl + fn + up` ): Next tab
- `ctrl l`: Clear terminal

### Shell scripts
starts with hashbang (`#!`) & reference to thing that runs the script e.g.
- `#! /bin/bash`: bash script
- `#! /usr/bin/env node`: node script

- [Beginners Bash Scripting](https://help.ubuntu.com/community/Beginners/BashScripting)

---

`ls -la | grep bash | sort nk1 > testfile`: ?

### Basic commands
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

`less filename`: Output file contents to screen, cf. more

`nano path/filename`: Open file in Nano editor ( ctrl + O to save, ctrl + X to exit )

`history`: Displays recent commands

`alias | wc -l`: Number of Aliases


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

### chown
'change owner' or group of object

### Disk Usage
- `df -h`
- `lsblk`
- `baobab`
- `du -hs ./path/to/dir` ( du = disk usage, h = human-readable, s = summary ) recursive summary of folder & subfolders..

### Installing / Uninstalling / Updating / Managing Applications

`sudo apt-get install packagename`: install a package/program

`sudo apt-get update`: update repo's

`sudo add-apt-repository ppa:numix/ppa`: add repository

`sudo apt-get autoremove`: remove dependencies for programs which are no longer installed

`ls /usr/share/applications | awk -F '.desktop' ' { print $1}' - > ~/Desktop/applications.txt`: list of installed applications


### Piping / Redirection
`sort deserts.txt | uniq > uniq-deserts.txt`: sort deserts.txt, pipe to `uniq`, redirect to newfile.

### Network tools
- `ifconfig`: configure a network interface [(x)](http://net-tools.sourceforge.net/man/ifconfig.8.html)
- `ping 8.8.8.8`: time to return answer
- `whois`: gets info on domain names or IP's
- `traceroute`: shows path to the destination IP
- `dig`: domain info groper, translates domains to ip addresses
- `iftop`: displays a table of bandwidth usage by hosts
- `whoami`: displays username
- `hostname`: displays hostname (name of computer)
- `nm-tool`: Network Manager Tool (Network Information)
- `ssh`: secure shell, 'ssh user@192.x.x.x'
- `lspci | grep Net`: info about Network Cards (wired & wireless)
- `lsusb`: info about USB devices connected etc.


----

### Other
`~/.bash_profile` (bash profile, used to store environment settings for terminal (source ~/.bash_profile activates changes))

` ~` (tilde) represents users home directory eg. `/home/user`, can use in paths e.g. `~/Documents/` is the same as `/home/user/Documents`

`$` represents prompt?

'alias' is another name for keyboard shortcut in the terminal, defined in .bashrc or .zshrc etc as `alias tek="cd ~Documents/tech"`

`.`: represents current directory

`..`: represents parent directory, `cd ..`: change to parent dir

`|` (pipe) pipes output of one command to another
