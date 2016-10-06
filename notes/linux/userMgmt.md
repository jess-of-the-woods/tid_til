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

### userdel
- `userdel userName`: delete user

### usermod
**examples**:
- `usermod -L userName`: lock an account
- `usermod -U userName`: unlocks
- `usermod -l new_username old_username`: modify the username of a user

### chfn
change real user name & information

### groups
see also '/etc/group'
- `groups`: will print list of all groups the user is in..
- `groups userName`

#### chgrp
change group ownership
- `chgrp cdrom fileName.md`: change ownership of 'fileName' to cdrom

### passwd
- `passwd userName`: sets a password for a user.
- `sudo passwd -e userName`: sets userName's password to expire so they must reset at next login

- [Linux and Unix passwd command](http://www.computerhope.com/unix/upasswor.htm)

---

See also [security](security.md)
