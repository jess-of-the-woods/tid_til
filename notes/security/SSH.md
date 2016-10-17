[network tools](../linux/network.md) | [linux security](../linux/security.md) | [security](security.md)

## SSH - secure shell

SSH daemon runs on port 22 by default.

syntax:

`ssh [user]@[ip address]` / `ssh [user]@[domain]`

e.g.

`ssh user@192.x.x.x` or `ssh user@mydomain.com`

**switches**
- `-i`: to specify a particular key (e.g. `ssh -i /home/user/.ssh/id_rsa_testgithub [user]@[domain]`)
- `-T`: test

### boilerplate config file for multiple keys:
 filename is 'config', lives in /home/user/.ssh
```bash
Host testgithub
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_rsa_testgithub

Host bitbucket
  HostName bitbucket.com
  User git
  IdentityFile ~/.ssh/id_rsa_bitbucket


```

- `ssh -T git@testgithub`: to test

- `git remote add origin git@testgithub:username/reponame.git`: add remotes to git repos

- `exit`: to logout

`find / -name sshd_config`: to find config file for SSH daemon

### SSH Keys
`ssh-keygen -t rsa`: to generate keys. '-t' to specify type

if using multiple keys, when asked what to name the newly generated keys, specify a name such as `id_rsa_github`

can either use a passphrase or not

`ssh -C 'email@email.com'`: '-C' is a comment

## Links
- [How SSH Works](https://www.youtube.com/watch?v=zlv9dI-9g1U) - YouTube (2 mins)
- [Setting up SSH Keys](https://www.youtube.com/watch?v=-J9wUW5NhOQ) - YouTube (14 mins)
