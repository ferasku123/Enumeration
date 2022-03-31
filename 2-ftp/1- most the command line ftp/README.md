ip attacker : 192.168.244.128

ip target : 192.168.244.132

------------------------------------------------------------

in this lab will learn some command in ftp

so will be create in target ip to allowed anonymous to change his folder and file home:

$`sudo mkdir -p /var/ftp/pub`

$`sudo chown nobody:nogroup /var/ftp/pub`

the nobody user and nogroup it is for guset anonymous users

$`echo welcome guset > /var/ftp/pub/test.txt`

$`echo admin-it > user.txt`

`$sudo mkdir /var/www/admin-it`

`$sudo chown admin-it:admin-it /var/www/admin-it`

`$sudo chmod 775 -R /var/www/admin-it`



int /etc/vsftpd.conf  put the line anon_root=/var/ftp/

and restart the ftp service 

$`sudo /etc/init.d/proftpd restart`






----------------------------------------------------------------


now lets enum in the attacker

login to the victime 

$`ftp 192.168.244.132`

`anonymous`

`anonymous`


<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/2-ftp/1-%20most%20the%20command%20line%20ftp/ftp%20anon%20users.png">

>`pwd`

>`ls`

>`cd pub`

>`ls`

for download this files test.txt and users.txt

>`get test.txt`

>`get `users.txt`

>`bye`

now if you want to show the files content



`$cat test.txt users.txt`


<img width="960" alt="keypad" src=https://github.com/ferasku123/Enumeration/blob/main/2-ftp/1-%20most%20the%20command%20line%20ftp/get%20file%20.png">

now the user admin-it will be brutforce in the ftp for you need to password for login to ftp 






