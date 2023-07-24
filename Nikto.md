a vulnerability scanner

`nikto -h 10.10.159.30`

`nikto -h 10.10.10.1 -Plugin apacheuser`

`nmap -p80 172.16.0.0/24 -oG - | nikto -h -`