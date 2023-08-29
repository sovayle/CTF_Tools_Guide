
Basic Filtering:
Syntax: `ip.addr == <IP Address>`
ip.addr == 239.255.255.250

Syntax: `ip.src == <SRC IP Address> and ip.dst == <DST IP Address>`
ip.src == 192.168.100.128 and ip.dst == 192.168.100.6

Syntax: `tcp.port eq <Port #> or <Protocol Name>`
tcp.port eq 60 or dcerpc


ARP:
check request reply packet and who it is being sent by]

ICMP:
0 for reply
8 for request

![[wireshark_color_codes.png]]


TCP Packet Analysis:
the sequence number and acknowledgment number.
port was not open because the acknowledgment number is 0.


DNS:
when analyzing DNS packets.

- Query-Response
- DNS-Servers Only
- UDP

If anyone of these is out of place then the packets should be looked at further and should be considered suspicious.


HTTP:
HTTP is used to send GET and POST requests to a web server in order to receive things like webpages

Some of the important information we can gather from the packet is the Request URI, File Data, Server.

Navigate to Statistics > Protocol Hierarchy.
This information can be very useful in practical applications like threat hunting to identify discrepancies in packet captures.



HTTPS:
Edit > Preferences > Protocols > TLS >  [+]

IP Address: 127.0.0.1

Port: start_tls

Protocol: http

Keyfile: RSA key location




When analyzing PCAPS we need to be aware of IOCs or Indicators of Compromise particular exploits may have with them. This is known as Threat Intelligence























