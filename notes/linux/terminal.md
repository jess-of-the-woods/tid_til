[backend](../backend.md) | [linux](index.md) | [tools](../tools.md)

## Nix Terminal (linux/unix)
- **[cron](cron.md)**
- **[BASH scripting](bash_scripting.md)**
- **[Git / Github](../git-github.md)**
- **[filesystem](filesystem.md)**
- **[network tools](network.md)**
- **[processes](processes.md)**
- **[searching](search.md)**
- **[security](security.md)**
- **[storage devices](storageDevices.md)**
- **[user management](userMgmt.md)**
- **[Vi / Vim](../vi.md)**

---

- [terminal keyboard shortcuts](#terminal-keyboard-shortcuts)
- [basic commands](#basic-commands)
  - [ls](#ls)
  - [cd](#cd)
  - [rm](#rm)
- [filters](#filters) (wc, sort, uniq, tee)
- [history](#history)
- [outputting](#outputting)
  - [piping](#piping)
  - [redirection](#redirection)
  - [standard streams](#standard-streams)
- text editors
  - [nano](#nanopico) (see also [Vi / Vim](../vi.md))
- [cut](#cut)
- [chmod](#chmod), [chown](#chown)
- [system](#system)
  - [help](#help)
  - [shell](#shell)
    - [environment variables](#environment-variables-env)
      - [PATH](#path)
  - [managing applications](#managing-applications)
    - [installing/uninstalling/updating/upgrading](#installinguninstallingupdatingupgrading)
    - [managing repositories](#managing-repositories)
  - [du](#du)
  - [aliases](#aliases)
  - [ln](#ln)
  - [shutdown](#shutdown)
  - [reboot](#reboot)
  - [archiving/compressing](#archiving--compressing) ([tar](#tar), [zip/unzip](#zip--unzip))
  - [tmux](#tmux-terminal-multiplexer)
  - [links](#links)

---

---

## terminal keyboard shortcuts
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
- `ctrl u`: clear line

## basic commands
- `pwd`: print working directory
- `clear`: clear screen (also ctrl + l)
- `mv`: move file(s), source file(s) then destination, e.g. `mv filename ~`
- `cp`: copy file(s), source file(s) then destination
- `touch`: creates empty file, `touch stuff.txt`
- `mkdir`: creates directory, e.g. `mkdir dirname`. `mkdir -p newfolder/child/chilOfChild` creates a path of folders (subfolders)
- `rmdir`: removes empty directories, e.g. `rmdir dirname`
- `file /user/home/filename.txt`: tells you document type

#### ls
- `ls` - list files
- `ls /bin`: list files/folders in /bin

**switches**:
- `-l`: long form
- `-a`: hidden files & directories
- `-t`: sort by time modified
- `-h`: human-readable

#### cd
change directory
- `cd ../..`: change directory up 2 levels
- `cd /` or `/` change directory to root
- `cd` goes to home

#### rm
remove files or directories e.g.
- `rm file1.txt`
- `rm -rf <dirname>`: removes non-empty directory

**switches**:
- `-r`: recursive
- `-f`: force

### filters
- `wc`: word count. lines, words, characters, eg. `cat filename | wc` or `cat filename | wc -l`: prints the number of lines in file
- `sort`: orders alphabetically, `sort filename.*` or `cat lakes.txt | sort > sorted_lakes.txt`
- `uniq`: filters out adjacent duplicate lines & outputs contents, `uniq filename`
- `tee`: outputs to screen & file. `who | tee wholist | wc -l`

### history
`history`: displays recent commands.
- `!23`: will enter (but not run) the 23rd command in history
- `history -c`: clears BASH history (stored in `~/.bash_history`)
- `rm ~/.zsh_history` or `echo "" > ~/.zsh_history`: to remove zsh history
- `!$` (bang-dollar): reuse the last argument(item) of previous command. e.g. if you run `mkdir test`, you can then type `cd !$` to reuse the last arg i.e. `test`
- `!*`: reuse all arguments except the first one (typically command name)
- `!!`: retype whole previous line

## outputting
- `cat`: outputs contents of file to terminal, `cat filename`
- `less`: Pager, Output file contents to screen page by page, e.g. `less filename`. see also 'more'
- `more`: prints out file to screen, page by page
- `head`: first 10 lines of a file, e.g. `head filename`
- `tail`: last 10 lines of a file. also `tail -f filename`: follows a file.. (as it changes over time)

### piping
`|` (pipe) pipes output (stdout / 1) of one command to the input (stdin / 0) of another (see basic commands for other examples)

Syntax:

`ps aux | grep nginx`: check CPU usage for a process (nginx)

`sort deserts.txt | uniq > uniq-deserts.txt`

sort deserts.txt, pipe to `uniq`, redirect to newfile.


### redirection
redirect output of a command to a file

`>`

Syntax:
- `cat filename > otherFilename`: outputs contents of filename to otherFilename (overwrites anything in otherFilename)
- `cat filename >> otherFilename`: append to file (instead of overwriting)

redirect output of a file to the input of a command

`<`

Syntax:
- `prog1 < file.txt`

e.g. `wc -l < testfile.txt`: redirect testfile.txt as the stdin for `wc -l` which will return (stdout) the number of lines in testfile.txt. equivalent to `cat testfile.txt | wc -l`

### standard streams
input/output/error
- 0 represents stdin or standard input
- 1 represents stdout or standard output
- 2 represents stderr or standard error

`ls -alh nonexistentFile 2> error.txt`: redirects error (stderr) returned from listing non-existent file to error.txt

---

### cut
if we have a file, file1.txt which contains:
```
user:we
user:love
user:linux
```

we can run `cat file1.txt | cut -d: -f2` which will output

```
we
love
linux
```
`-d`: delimiter, `-f2`: second field

#### Nano/Pico
- `nano path/filename`: Open file in Nano editor ( ctrl + O to save, ctrl + X to exit ) - [beginners guide](http://www.howtogeek.com/howto/42980/the-beginners-guide-to-nano-the-linux-command-line-text-editor/)

### chmod
'change mode' change the access permissions to file system objects (files and directories).
- `chmod`: change mode, modify permission string
- `chmod +x`: adds execution rights
- `chmod -x`: removes execution rights

`chmod 644 filename` or `chmod 777 filename`

see also [file permissions](file_permissions.md) | [user management](userMgmt.md)

### chown
'change owner' or group of object
- `chown -R ghost:ghost .` chown recursively, group: ghost, user:ghost, `.` is current dir

## xargs
build & execute command lines from standard input. apply a command to each element of stdin..
e.g.
- `seq 5 | xargs -n 1 echo "hello"`: will print out hello before each number from 1-5
- `ls | xargs -n 1 chgrp cdrom`: change group of all files piped from ls to the group cdrom
- `find / -name .conf | xargs -I{} -n 1 chgrp cdrom {}`: find files (starting at `/`), with '.conf' in the name, pipe to xargs & chgrp to cdrom for each file found. (don't do this!, just an example of how to structure a command)

## system
- `$`: represents prompt in BASH
- `.`: represents current directory
- `..`: represents parent directory, `cd ..`: change to parent directory
- ` ~`: (tilde) represents users home directory eg. `/home/user`, can use in relative paths e.g. `~/Documents/` is the same as `/home/user/Documents`
- `~/.bash_profile`: used to store environment settings for terminal (source ~/.bash_profile activates changes))

### help
- 'man': manual pages. Use like: `man ls` or `man uniq` for manual pages on the ls or uniq commands
- help. to get help on a command type `commandName --help`, e.g. `ls --help` for help on ls
- `whatis`: displays one-line manual page descriptions. e.g. `whatis grep`
- `which <command>` e.g. `which ls`: locates a command (the path to where it is found)
- `whereis`: locate the binary, source & man pages for a command

### system commands
- `tty`: displays the virtual terminal you are using..
- `whoami`: displays username
- `logname`: Prints the users login name
- `who am i`: displays username & terminal you are in.
- `w`: shows who is logged in & what they are doing
- `hostname`: displays hostname (name of computer)
- `uname`: print system information. `uname -a` prints all, `uname -r`: prints kernel version
- `lsb_release -a`: print distribution-specific information (find out ubuntu (or any distro) version)
- `service udev status`: Check if 'udev' service is running (on older machines)
- `systemctl status udev`: Check if 'udev' service is running (on newer machines)

### shell
- `echo $0`: print the name of the shell you are using
- `echo $SHELL`: print the location of the shell you're using
- `echo "$$"`: to find the process ID (PID) of the current instance of shell
- `bash`: to change to BASH shell, `zsh`: to change to zsh shell (if installed)
- `chsh -s /bin/zsh`: change login shell to zsh

#### environment variables (env)
- `env`: prints a list of environment variables
- `set`: prints all variables

##### PATH
`env | grep PATH` or `echo $PATH`: to see the PATH

`export PATH=$PATH:/usr/sbin`: to add /usr/sbin to PATH

A users PATH is stored in `~/.bash_profile`. To add a directory to the PATH permanently, add it to the line in .bash_profile that starts with PATH with a colon separated list of absolute paths.

- [What is PATH?](http://www.linfo.org/path_env_var.html)
- [add directory to PATH](https://askubuntu.com/questions/60218/how-to-add-a-directory-to-my-path)

### managing applications
- 'APT' - Advanced Package Tool (similiar to aptitude)
- 'PPA' - Personal Package Archives

#### installing/uninstalling/updating/upgrading
- `apt-cache search searchterm`: search repositories for search term (search through package names & descriptions)
- `sudo apt-get install packagename`: install a package/program
- `sudo apt-get remove packagename`: remove a package/program
- `sudo apt-get update`: update repo's (retrieve new lists of packages)
- `sudo apt-get upgrade`: install updates
- `sudo apt-get autoremove`: remove dependencies for programs which are no longer installed
- `ls /usr/share/applications | awk -F '.desktop' ' { print $1}' - > ~/Desktop/applications.txt`: list installed applications & output to file on desktop

- `dpkg -L packagename`: lists all files 'owned' by a package

#### managing repositories
- `sudo add-apt-repository ppa:numix/ppa`: add repository
- `/etc/apt/sources.list` & any file with the suffix '.list' in `/etc/apt/sources.list.d/`: displays repositories subscribed to

### du
disk usage, estimate file space usage (see also [df](storageDevices.md#df))
- `du -hs ./path/to/dir`

**switches**:
- `h` = human-readable
- `m` = display in megabytes
- `s` = summary (recursive summary of folder & subfolders..)
- `-d 1`: display 1 level deep



### aliases
- 'alias' is another name for keyboard shortcut in the terminal, defined in .bashrc or .zshrc etc as
- `alias tek="cd ~Documents/tech"`
- `alias | wc -l`: number of aliases

### ln
creates links to files or folders
- `ln file1 yea`: creates hard link to file1. link is called yea
- `ln -s file1 yea`: creates symlink (soft) to file1. If file1 is deleted, link will not work..
- [more info](http://www.unixtutorial.org/commands/ln/)

### shutdown
`shutdown`: shuts the system down
- `shutdown -h`: halt/turn off.
- `shutdown -h now` or `poweroff` or `init 0`: turn off now

### reboot
- `shutdown -r +30`: reboot in 30 minutes,
- `init 6` or `reboot`: reboot computer

### archiving / compressing

#### tar
**switches**:
- `-c`: create an archive
- `-f`: specify a filename
- `-t`: list the contents of archive
- `-v`: operate verbosely
- `-x`: extract
- `-z`: gzip

**examples**:
- `tar -cf archive.tar file1 file2`: Create archive 'archive.tar' containing files file1 and file2.
- `tar -tvf archive.tar`: List the files in the archive 'archive.tar' verbosely.
- `tar -xf archive.tar`: Extract the files from archive 'archive.tar'.
- ([more info](http://www.computerhope.com/unix/utar.htm))

#### zip / unzip
- `zip -r zippeddocs.zip Documents/`: zip Documents dir into an archive called zippeddocs.zip
- `unzip zippeddocs.zip`: unzip archive into current dir

see also [gnupg](security.md#gnupg-gpg)

### tmux (terminal multiplexer)
- `tmux`  to enter tmux
- `ctrl + b` then `?` for help (list commands)
- `ctrl + b` then `c` to create new window (`p`: previous, `n`: next, `w`: list all)
- `%`: split horizontally, `"`: split vertically
- `exit`: to exit

---

## Links
[List of Unix commands](https://en.wikipedia.org/wiki/List_of_Unix_commands) - Wikipedia

<!-- See also  -->
