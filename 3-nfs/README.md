
<h3>ip server victime</h3> : 192.168.244.132

<h3>ip client attacker</h3> : 192.168.244.133

tcp udp port 2049

tcp udp port 111

<h3>file configration</h3>:  /etc/sysconfig/nfs

the nfs it is sharing data in network  it is fast and easy but not secure because there is not authenication so there is not usename and password 

-------------------------------------------------------------------------

<h3>setup server</h3> : for shared folder /data why must edit the file /etc/exportfs and put :




<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/3-nfs/file%20exportf.png">

/data       *(rw,root_squash)


<h3>/data</h3> this is folder  

<h3>*</h3> it is mean all the network or you can replace wih your ip client or network ips range as 192.168.244.0/24 
 
 the <h3>rw</h3> it is mean read and write , <h3>ro</h3> it is mean read only 

<h3>root_squash</h3> Whether it is written or unwritten it is by the defaulet ,
it is assumed to be for solate the root user of the client from the root user of the server

now you must reload nfs-service

#`exportrf -rf`



-----------------------------------------------------------

<h3>client</h3>



<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/3-nfs/client%20share.png">

for to view the share folder in nfs:


#`showmount -e 192.168.244.132`   # ip server nfs

and now you must create a folder for share :

#`mkdir /share`

#`mount -t nfs 192.168.244.132:/data /share`

for to view mount folders:

#`df -h`





If you want to create a mount folder permanently you can add in the /etc/fstab:


<img width="960" alt="keypad" src="https://github.com/ferasku123/Enumeration/blob/main/3-nfs/fstab.png">

192.168.244.132:/data       /share       nfs    _netdev 0 0   

#_netdev  The filesystem resides on a device that requires network access (used to prevent the system from attempting to mount these filesystems until the network has been enabled on the system). 









