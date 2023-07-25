HASH: df8287309c06b3395f14145fd49fc4088d1236425c71f13a0efc38602de23f90

`john [options] [path to file]`

`john --wordlist=[path to wordlist] [path to file]`

john --wordlist=/usr/share/wordlists/rockyou.txt hash_to_crack.txt

`john --format=[format] --wordlist=[path to wordlist] [path to file]`

john --format=raw-md5 --wordlist=/usr/share/wordlists/rockyou.txt hash_to_crack.txt

`john --list=formats`

`john --list=formats | grep -iF "sha"`

`john --format=NT --wordlist=/usr/share/wordlists/rockyou.txt /home/kali/Scripts/ntlm.txt`

`unshadow [path to passwd] [path to shadow]`

**Example Usage:**

unshadow local_passwd local_shadow > unshadowed.txt

`john --single --format=[format] [path to file]`

**Example Usage:**

john --single --format=raw-sha256 hashes.txt

/etc/john/jon.config

read john rules

zip2john

`zip2john [options] [zip file] > [output file]`

**Example Usage**

zip2john zipfile.zip > zip_hash.txt

zip2john secure.zip > zip_hash.txt

john --wordlist=/usr/share/wordlists/rockyou.txt zip_hash.txt

rar2john

ssh2john



