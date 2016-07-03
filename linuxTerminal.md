[Notes](notes.md)

##Nix Terminal

###Terminal window shortcuts
- `ctrl alt t`: Open terminal window
- `ctrl shift t`: Open new tab
- `ctrl shift n`: Open new window
- `ctrl shift w`: Close tab
- `ctrl shift q`: Close terminal window
- `ctrl pageup` ( `ctrl + fn + up` ): Next tab
- `ctrl l`: Clear terminal

###Shell scripts
starts with hashbang (`#!`) & reference to thing that runs the script e.g.
- `#! /bin/bash`: bash script
- `#! /usr/bin/env node`: node script

[Beginners Bash Scripting](https://help.ubuntu.com/community/Beginners/BashScripting)

_________________

`history` ( displays recent commands )

`alias | wc -l` ( Number of Aliases )

`wc` ( Word Count )

`ls -la | grep bash | sort nk1 > testfile`: ?

###Disk Usage
- `df -h`
- `lsblk`
- `baobab`
- `du -hs ./path/to/dir` ( du = disk usage, h = human-readable, s = summary ) recursive summary of folder & subfolders..

###ls
- `ls` - list files (`-l` long form, `-a` hidden files & directories, `-t` sort by time modified)
- `ls /bin`: list files/folders in /bin

###rm
- `rm` ( remove files & directories, -r recursive )
- `rm -rf dirname`: removes non-empty dir ( recursive & force )

`pwd`: print working directory

`cd ../..`: change directory, `cd /` goes to root (as does `/`), `cd` goes to home

`clear`: clear screen

`mv` (move file(s), source file(s) then destination)

`cp`: copy file(s), source file(s) then destination

`touch filename.*`: creates empty file

`mkdir dirname`: creates directory

`cat`: outputs contents of file to terminal, cat filename

`wc`: lines, words, characters, eg. `cat filename | wc`

`sort`: orders alphabetically, `sort filename.*` or `cat lakes.txt | sort > sorted_lakes.txt`

`uniq`: filters out & adjacent duplicate lines & outputs contents, uniq filename

`grep`: global regular expression print, grep -i case insensitive, grep -R recursive, 'grep -R searchterm /home/user/'

`sed`: stream editor, accepts standard input and modifies it based on an expression, before displaying it as output

`file /user/home/filename.txt`: tells you document type

`less filename`: output file contents to screen, cf. more

###chmod
- `chmod`: change mode, modify permission string
- `chmod +x`: adds execution rights
- `chmod -x`: removes execution rights

`chown`: change owner or group of object

---

`nano path/filename`: open file in nano editor ( ctrl + O to save, ctrl + X to exit )

`sudo apt-get install packagename`: install a package/program

`sudo apt-get update`: update repo's

`sudo add-apt-repository ppa:numix/ppa`: add repository

`sudo apt-get autoremove`: remove dependencies for programs which are no longer installed

`ls /usr/share/applications | awk -F '.desktop' ' { print $1}' - > ~/Desktop/applications.txt`: list of installed applications


###Piping/redirection
`sort deserts.txt | uniq > uniq-deserts.txt`: sort deserts.txt, pipe to `uniq`, redirect to newfile.

###Network tools
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

`~/.bash_profile` (bash profile, used to store environment settings for terminal (source ~/.bash_profile activates changes))

` ~` (tilde) represents users home directory eg. `/home/user`

`$` represents prompt?

'alias' is another name for keyboard shortcut in the terminal

`.` (dot) represents current directory

`..` (dot dot)represents parent directory

`|` (pipe) pipes output of one command to another
