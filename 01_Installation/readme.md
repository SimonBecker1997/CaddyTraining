# Installation of Caddy
## Install Caddy on Ubuntu
Run the following commands, one after another, to install Caddy on Ubuntu:
```
sudo apt install -y debian-keyring debian-archive-keyring apt-transport-https
curl -1sLf 'https://dl.cloudsmith.io/public/caddy/stable/gpg.key' | sudo gpg --dearmor -o /usr/share/keyrings/caddy-stable-archive-keyring.gpg
curl -1sLf 'https://dl.cloudsmith.io/public/caddy/stable/debian.deb.txt' | sudo tee /etc/apt/sources.list.d/caddy-stable.list
sudo apt update
sudo apt install caddy
```
## Install Caddy on RHEL, CENTOS
For CENTOS, Redhat run the following Commands
```
dnf install 'dnf-command(copr)'
dnf copr enable @caddy/caddy
dnf install caddy
```

Official Docs: https://caddyserver.com/docs/install#debian-ubuntu-raspbian
