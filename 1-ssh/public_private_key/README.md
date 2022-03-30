attacker ip : 192.168.244.128

target ip : 192.168.244.132


-----------------------------------------------------

the  public key and private key it must login by the file not bye the password:

you must the now create public and private key in attacker machine:

$`ssh-keygen -t rsa`



<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/1-ssh/public_private_key/create%20public%20private%20key.png">

now will be create hidden folder  in  /$HOME/.ssh :

will be content the file 


<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/1-ssh/public_private_key/privte%20and%20public.png">

the file id_rsa this is private key this is must be read by the owner and the root only

the file id_rsa.pub this is public key it must on the target machine for loggin without password

if you can permssion on the target on the home user admin-it you can login with public key , you must create a hidden folder in the /$HOME  with name is .ssh
and it must in here file public key the attacker machine with name authorized_keys in /$HOME/.ssh

in attacker machine :


<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/1-ssh/public_private_key/copy%20public%20key%20to%20target%20machien.png">


and in the victime machine 


<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/1-ssh/public_private_key/authorized_keys.png">

now the public key of user feras on the target machine in the home user the admin-it , 
now will be login to the admin-it without password from the attacker mahcine user feras:


<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/1-ssh/public_private_key/login%20with%20public%20key.png">



-------------------------------------------------------------------------------------------------------------------------------------------

<h3>loggin with private key for targe machine</h3>:

if you found the private key for  target machine  will be can with this key:

now the private key for admin-it in target machine will be found in the web service



<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/1-ssh/public_private_key/private%20key%20root.png">

now will be download this file in the attacker machine

$`mkdir private_key`

$ `cd private_key`

$`wget 'http://192.168.244.132/id_rsa'`

$`chmod 777 id_rsa`

$`ssh -i id_rsa admin-it@192.168.244.132`


<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/1-ssh/public_private_key/login-with-private%20key.png">





