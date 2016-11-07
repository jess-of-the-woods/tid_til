[terminal](terminal.md) | [security](security.md)

## user account management

### users
prints the user names of users currently logged in to the current hostname

### useradd
- `useradd userName`: creates a user.
e.g. `useradd mymble -m -d /home/mymble -s /bin/bash`

**switches**:
- `-m`: create a home directory
- `-d`: define a path for it
- `-s`: specify default shell

`sudo adduser userName cdrom`: add userName to cdrom group

### userdel
- `userdel userName`: delete user
- `sudo deluser --remove-home userName`: delete 'userName' user & home directory & mails
- `sudo deluser --remove-all-files userName`: delete 'userName' & all files owned by this user on whole system

### usermod
**examples**:
- `usermod -L userName`: lock an account
- `usermod -U userName`: unlocks
- `sudo usermod -a -G nurses mom`: add (append `-a`) mom to the nurses group. `-g` will change the primary group (i.e. remove her from mom group), `-G` will just add her to a new group, but not change the primary group
- `usermod -l new_username old_username`: modify the username of a user

### chfn
change real user name & information
`chfn -f seagull userName`: change userName's full name to 'seagull'

### groups
see also '/etc/group'
- `groups`: will print list of all groups the user is in..
- `groups userName`

#### groupadd
create a new group
`sudo groupadd cyborg`: creat a group named 'cyborg'

#### chgrp
change group ownership
- `chgrp cdrom fileName.md`: change ownership of 'fileName' to cdrom

### passwd
- `passwd userName`: sets a password for a user.
- `sudo passwd -e userName`: sets userName's password to expire so they must reset at next login

- [Linux and Unix passwd command](http://www.computerhope.com/unix/upasswor.htm)

---

## links
- [A command to list all users? And how to add, delete, modify users?](https://askubuntu.com/questions/410244/a-command-to-list-all-users-and-how-to-add-delete-modify-users)

See also [chown](terminal.md#chown) | [chmod](terminal.md#chmod)
