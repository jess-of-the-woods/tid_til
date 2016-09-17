[DevOps](index.md) | [server-side](../server-side.md)

## nginx setup

- create a droplet
- SSH in
- `apt-get update`
- `apt-get upgrade`
- `apt-get install vim curl build-essential python-software-properties git-core -y`

### add user
- `addgroup admin`
- `adduser deployer --ingroup admin`, then provide a new password
- `ssh-copy-id deployer@123.456.789.123` will copy public ssh key to server & authorise pc to login
- `sudo add-apt-repository ppa:nginx/stable`
- `sudo apt-get update`
- `sudo apt-get install nginx`
- `sudo service nginx start`
- try accessing IP from browser
- `cd /etc/nginx/sites-enabled`
- `vi default`: config file (server-block)
- `cd /usr/share/nginx/html`

based on [tutorial](https://www.youtube.com/watch?v=TIaBrUo2944&index=3&list=PLjQo0sojbbxUav7I746f0lT4apGX8-iON) - Codemy, YouTube



<!-- ---

See also -->
