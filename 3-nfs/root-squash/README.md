
now i am a root in client  , you have 2 root in folder /share root for server and  root for client and the permsission share is rw for all the network

but there is a problem

client#`cd /share`

client#`ls -la`

client #`touch myfile`


<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/3-nfs/root-squash/problem.png">


permsision denied Although there is read and write (rw) permission for the share on the server 

why? 

because the /data folder in server the presmission is drwxr-xr-x

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


-----------------------------------------------------------------------------------------------

It is assumed that the root user on the client can change the attributes inside the share folder, such as changing the name, deleting, modifying the validity and others.



client#`chmod 777 1`

<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/3-nfs/root-squash/perms.png">

but the deny because the system in server used in file /etc/exports root_squash


server#`cat /etc/passwd | grep "nfs"`


server#`cat /etc/exports`


<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/3-nfs/root-squash/root-squash.png">

the server is used the root_squash in folder /data as nobody user  false shell

if you want to  disabled root_squash in /data ,you must replace to 

/data    *(rw,no_root_squash)



and reload the service nfs:

server#`exportfs -rf`

-----------------------------------

and now if go to client root:

client#`chmod 777 1`

client#`mkdir client-root`

client#`ls -la `


<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/3-nfs/root-squash/finish.png">




