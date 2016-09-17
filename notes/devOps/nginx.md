[DevOps](index.md) | [server-side](../server-side.md)

## nginx

### setup

- create a droplet
- SSH in
- `apt-get update`
- `apt-get upgrade`
- `apt-get install vim curl build-essential python-software-properties git-core -y`

#### add user
- `addgroup admin`
- `adduser deployer --ingroup admin`, then provide a new password


- `ssh-copy-id deployer@123.456.789.123` will copy public ssh key to server & authorise pc to login
- `sudo add-apt-repository ppa:nginx/stable`
- `sudo apt-get update`
- `sudo apt-get install nginx`
- `sudo service nginx start`
- try accessing `123.456.789.123` (I.P) from browser
- `cd /etc/nginx/sites-enabled`
- `vi default`: config file (server-block)
- `cd /usr/share/nginx/html`

based on [tutorial](https://www.youtube.com/watch?v=TIaBrUo2944&index=3&list=PLjQo0sojbbxUav7I746f0lT4apGX8-iON) - Codemy, YouTube

## config

- ssh in as deployer
- `cd /opt`
- `sudo mkdir www`
- `sudo chgrp -R admin www`: set www directory to be owned by admin group
- `sudo chmod -R g+rwxs www`: set permissions to be read-write-execute for members of admin group
- `cd www`
- `mkdir cheqin.me`: use domain as directory name
- `cd cheqin.me`
- `vi index.html` & create a basic html file
- `cd /etc/nginx/sites-available`
- `sudo vi cheqin.me`: to create new server-block

```sh
server {
  listen 80;
  server_name www.cheqin.me;
  access_log /opt/www/cheqin.me/access.log;

  root /opt/www/cheqin.me;
}
```


- `cd ../sites-enabled`: sites-enabled only has symlinks to sites-available
- `sudo ln -s /etc/nginx/sites-available/cheqin.me cheqin.me`: to create symlink to new site
- `sudo service nginx restart`
- try accessing site through domain

- prepend the following to `/etc/nginx/sites-available/cheqin.me`

```
server {
  listen 80;
  server_name cheqin.me;
  return 301 $scheme://www.cheqin.me$request_uri;
}
```

`$scheme` & `$redirect_uri` are nginx variables. `$scheme` which will pass in either http:// or https://. $redirect_uri will pass in what ever uri that comes after the domain, e.g. cheqin.me/page1

- `sudo service nginx restart`

nginx error messages kept in `/var/log/nginx`

<!-- ---

See also -->
