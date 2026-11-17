```bash
apt update -y
apt upgrade -y 
apt full-upgrade -y
```
Seit Trixie gibt es eine neue sources.list im deb822-Format. Zum konvertieren:  
`apt modernize-sources`

Die Packetquellen von Sury kann man so hinuzfügen  
```bash
apt-get -y install lsb-release ca-certificates curl
curl -sSLo /tmp/debsuryorg-archive-keyring.deb https://packages.sury.org/debsuryorg-archive-keyring.deb
dpkg -i /tmp/debsuryorg-archive-keyring.deb
sh -c 'echo "deb [signed-by=/usr/share/keyrings/debsuryorg-archive-keyring.gpg] https://packages.sury.org/php/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/php.list'
apt-get update
```
