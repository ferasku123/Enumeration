if you want to secure your ssh

1-must to be convert the port number from 22 to any number

2-deny the login to root from remoet with add the line in file /etc/ssh/sshd_config

PermitRootLogin no

3-deny any login with password in with add the line in file /etc/ssh/sshd_config

PasswordAuthentication no

4-permit the login to ssh with one ip , the ip admin is only login to ssh server

first in file /etc/hosts.deny , add line 

sshd: ALL

and in the file /etc/hosts.allow

add the ip you must login into the server with line

sshd: 192.168.244.1

5-last restart ssh service

systemctl restart ssh


6- if you want to login with password you must secure ssh with port khnow_x and firewall and PAM with delay login and stop the brutforce attack and you must use

/etc/hosts.allow

/etc/hosts.deny





