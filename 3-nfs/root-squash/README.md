
now i am a root in client  , you have 2 root in folder /share root for server and  root for client and the permsission share is rw for all the network

but there is a problem

client#`cd /share`

client#`ls -la`

client #`touch myfile`


<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/3-nfs/root-squash/problem.png">


permsision denied Although there is read and write (rw) permission for the share on the server 

why? 

because the /data folder in server the presmission is -rw-r--r-- 

#`ls -ld /data`


<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/3-nfs/root-squash/cause.png">

whats happends ,the happeneds is the other do not use the write prismmsion 

********       *******    ************   ********           ************
client    ->    rw     ->     r             -> r            server   
                share      permsisson
             
********       *******    ************   ********           *************


so in the end will get the read only 

so you must the others users  get the write permsiion in server

server#`chmod o+w /data`

<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/3-nfs/root-squash/soul.png">

and if you want to go to client

client#`touch myfile`

cleint#`ls -l`

<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/3-nfs/root-squash/res.png">

now it is create 




