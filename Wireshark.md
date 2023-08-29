
Basic Filtering:
Syntax: `ip.addr == <IP Address>`
ip.addr == 239.255.255.250

Syntax: `ip.src == <SRC IP Address> and ip.dst == <DST IP Address>`
ip.src == 192.168.100.128 and ip.dst == 192.168.100.6

Syntax: `tcp.port eq <Port #> or <Protocol Name>`
tcp.port eq 60 or dcerpc


ARP:
check request reply packet and who it is being sent by