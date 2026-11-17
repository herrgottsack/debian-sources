```bash
apt update -y
apt upgrade -y 
apt full-upgrade -y
```
Seit Trixie gibt es eine neue sources.list im deb822-Format. Zum konvertieren:  
`apt modernize-sources`
