
<h3>ip attacker: 192.168.244.128</h3>


<h3>ip target: 192.168.244.132</h3>

-------------------------------------------
ftp: port 21 

for scan port ftp in nmap:

$`nmap -sV -p 21 192.168.244.132`


<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/2-ftp/nmap%20classic%20in%20ftp.png">

now if you full scan for ftp service:

#` ls -l /usr/share/nmap/scripts/ | grep "ftp"`


<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/2-ftp/nmap%20file%20script%20ftp.png">


#`nmap -sS -p 21 --script ftp-anon,ftp-syst,ftp-vsftpd-backdoor 192.168.244.132`

<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/2-ftp/nmap%20full%20scaan.png">

-------------------------------------------------------------------------------------------------------------------------
this ftp is allowed anonymous(guset) users 

to login in the ftp with anonymous :

#`ftp 192.168.244.132`

`anonymous`      /////this user name

`anonymous`      /////this is password

`help`


<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/2-ftp/ftp%20login.png">









