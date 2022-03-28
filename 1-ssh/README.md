<h3>ip attacker</h3>: 192.168.244.128

<h3>ip victime</h3>: 192.168.244.132

---------------------------------------------
<h3>ssh or sshd or openSSH </h3>:
this is allow the open remote shell 

<h3>defuale port number is 22</h3>

------------------------------------------------------------

for the enumeration with nmap from attacker

#`nmap -sV  -p 21 192.168.244.132`


<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/1-ssh/nmpa.png">


--------------------------------------------------------------------

in the attacker machine this is config file ssh:

$`nano /etc/ssh/sshd_config`


<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/1-ssh/3-msfadmin%20ssh.png">


----------------------------------------------------------------------------

if you want to access in msfadmin from  attacker remote you username: msfadmin and password:msfadmin and ip target : 192.168.244.132

#`ssh msfadmin@192.168.244.132`


<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/1-ssh/msfadmin ssh.png>

                                   
                                   
now you are in attacker machine with msfadmin user
                                   



