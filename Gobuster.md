`gobuster dir -u http://10.10.10.10 -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt` 

`gobuster dir -u http://10.10.252.123/myfolder -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -x.html,.css,.js'

-k flag to bypass HTTPS instead of http
-d -w common
-t 64
`gobuster dns -d mydomain.thm -w /usr/share/wordlists/SecLists/Discovery/DNS/subdomains-top1million-5000.txt`

`gobuster dir -u 10.10.70.44 -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -t 64`

`gobuster dir -u 10.10.70.44/Changes -w /usr/share/wordlists/dirbuster/directory-list-2.3-small.txt -t 64 -x.html,.css,.js,.conf,.txt`

`gobuster vhost -u http://example.com -w /usr/share/wordlists/seclists/Discovery/DNS/subdomains-top1million-5000.txt`