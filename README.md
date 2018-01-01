# Linux_Basics
Complete understanding of Linux base for a DevOps Engineer 

                              Hardware <----> Operating systems <----> Software

  In order to communicate Hardware with Software we need an Operating systems, this is for Example Linux O.S, Windows O.S etc ..

  So this Linux O.S has a different distributions like Redhat Linux O.S, Ubuntu Linux O.S, Fedora Linux O.S. Everything are the distributions of Linux O.S

  Note: If you have any problem with Redhat Linux O.S, if you call the Ubuntu Linux O.S They won't slove your problem. Only which distribution version that you are using if you call that they will slove the problem and your issue.

OPENSOURCE: 

  Note : Many people say open source is for free. That's not the right word to speak, The right way of opensource defination is below.

  Open source mean many companies like mysql, Dynomodb, amazon, gives the opensource software to view there source code for free, but not to modify that source code. If you wan't to do there will be an Licencing aggrement, Maintence contract, Expensive while we using this in the production level.

THE SHELL: 

  Means intracts with Operating system that we can intract with. Either in Server U.I, or G.U.I.
  
  In linux we have Line User Interface. Shell is a screen to intract with Operating systems.
  
USERS:

  ROOT USER: Highest level of the Operating system, where our Opearating system is stored.

  USER's : where we have the Home folder that we can store, download pictures, videos etc ..

CAPITALIZATION:

  In windows : Home, home, HOME, homE in all the cases it works. Capitalization doesn't matters.

  In Linux O.S: HOME,home, Home, homE here it won't work, becausee Capitalization matters.


SERVER Vs DESKTOP:

  For Example in Linux O.S we have a Distribution of Redhat Linux O.S, this Redhat Linux O.S has two distributions like Server version, Desktop version.

  In the server distribution version we can only see terminal.

  In the Desktop version we can see everything.

WHY LINUX ?

  Because its has a secure in terms of servers, we have many opensource versions, we have a highest level of ROOT user for security, download an install any thing like utilites etc ..

==============================================================================================================================


TCP/IP : 

   Version : IPv4, IPv6. Still now mainly we are using IPv4

  TCP : Transmission control protocal, Routable Protocal.
  IP: Internet Protocal, has Routing, Subnet Masking, Default Gateway.
  
 In TCP/IP there is a concept called Windowing. what it exactly mean is that it sends the data into Packets from computer one to computer 2. After computer 2 recives the packet one it sends an Acknowledgement to computer one, then the computer send two packets, then four packetes, then eight packets, for every packet the computer two receives it sends an Acknowledgement. For Example if the computer one send to fail in the middle, so again the computer one will look at the last acknowlegdement that has been sent from the computer two then it resend by sending from that particular packet, and the same cycle repeats .......
 
 For Example: The packets sends in this format below
 
   1 2 4 8 16 32 64 128 ...............................
   
 IPAddress for all the default is ( Also is called Static)
 
              192.168.1.55 --> Default IPAddress
              255.255.255.0 --> Subnet Masking
              192.168.1.1 --> Default Gateway
              192.168.1.1 --> DNS Server
              208.55.44.1 --> Other IPAddress.
              
DHCP Client:
 
   Why this means, our operating system will renewel or Lease the IPAddress from this Client so that there is no need to put all the above IP addresses. Linux O.S has a specaility that for everything the IPAddress is rentead, when it reach a mark of 50% days or years it will send an Acknowledgement to the DHCP client. So this Client will Extend this Lease again, like that the process goes extending extending extending ................ Also called as Dynamic
   
NAT : 
 
  Network Address Transmission gives a Unique IP address for the Router. This IP Address won't be used any where in the world and will be Unique.
  
OCTECKS : 

  For Each IP Address is divided into four Octecks. Each Octeck will be in the range of 256= 2 ^ 8.
  
SUBNET MASKING:

  It differentiates that what part of the IP Address is from the Network IPaddress, and what part of the IPAddress is from the Computer. 
 Dependes upon the requirement we can change.
 
  Note: Important to know is below the types of subnets:
  
              A class Subnets ----------> 255.0.0.0
              B class Subnets ----------> 255.255.0.0
              C class Subnete ----------> 255.255.255.0 
              
   So if any one commes and say to give the address for Class C Network about a range of 198. Solution is : 255.255.255.198
   
 ===============================================================================================================================
 
LINUX COMMANDS: 

  SUDO: Super user do. Everything that has to start to use sudo for the root user to perform.
  
  Man: The command is shown below 
  
              man < ping > --> Shown the complete information pages of the ping command.
              
  taskel : In root of the UBUNTU we have a tasksel command, that can install the webservers with a single checkpoint what ever is there.
  
  
              sudo tasksel    ------> Note: Hit space bar for checkpoint.
              
              
   apt-get : Its a linux version. what it does is that it goes to the linux repository and get the particular installation what we need and install in our computer.
   
              sudo apt-get install < Anything we need >
              
              sudo apt-get remove < Anything we need>
              
              suod apt-get upgrade ----> checks for latest version and upgrade.
              
   SERVICES: If we are changing the configuration files of a server or webserver we has to restart the service, other wise we can't get changes we have made in the configuration file. Below is the Example for the service restarting for apache2 after changing the config file.
   
              sudo /etc/init.d/apache2 start
              sudo /etc/init.d/apache2 stop
              sudo /etc/init.d/apache2 restart
              
   TOP: Command that shows all the running processes, CPU usasage, Memory. we can also kill the processes by simply typing " k " and "PID number". need help can type " h "
   
              sudo top
   
   CHOWN: Change ownership, if we want to change the ownership of the file or folder simply use the commands below:
   
              sudo chown root <filename>
              sudo chown root <foldername>
              
              sudo chown <username> <filename>
              sudo chown <userrname> <foldername>
   
   EDIT & VALIDATING: 
   
              :/name        --> we can find all the info related to name.
              :/*name*      --> we can find all the name in the top of the file.
              :/?name       --> can see the name info at the end of the file.
              :e < Path of the new file >  -----> If we are in the vim editor and want to see the new file can use this cammand and make changes.
              :q!        --> Force quit.
              :wq         --> saving the file
              :w <filename>   ---> want to rename the file, SAVE AS.
              
             
  NAVIGATING in Linux:
  
              ls -l ---> shows the long listing information.
              ls -m --> shows the list in comms on after one.
              
  FIND a file or folder in the O.S:
  
              sudo find -iname *filename*
              sudo find -iname *foldername*
              
              sudo find -iname php*  --> shows all the files start with php, with path information.
              
              sudo find -iname *.config ---> shows all the congiguration files in the root.
    
    Note: While using this command be sure that you are in the root directory. otherwise it won't display anything.
    
 RENAME, COPY, MOVE files or folders:
 
              sudo cp <filename1> <filename1.bak>
              
              sudo cp <test1> <test1.bak> -R  --> If its a Directory, want to backup a directory.
              
              sudo rm <test1> -R ---> Removes a directory.
              
              sudo rm - rf <test1> --> want to remove a directory containes files in it.
              
              
 MOUNTING DRIVES: 
 
   If we want to mount a drive we has to fallow the commands as fallows. Shows how to mount a drive.
   
              sudo mkdir /mnt/drive
              
              sudo fdisk -l ---> Shows all the hard drive Information.
              
              sudo mount /dev/xvdal /mnt/flashdrive --> mount all the files from /dev/xvdal to /mnt/flashdrive
              
              sudo umount /dev/xvdal /mnt/flashdrive --> For unmount the drive, no changes will be happened.
              
===============================================================================================================================


USERS, ADD'S, DELETE USERS :

            sudo adduser <username>  --> Adds an user 
            
            sudo delete <username>   --> Delete the user
            
   Note that we can make sure by checking is our user is added or not in the fallowing below directory
   
            sudo vim /etc/passwd     --> displays all the users, root, information

  Want to change the password of the user, use below command:
  
            sudo passwd <username>
            
  If we want to rename for the user that is already exist simply go to the " sudo vim /etc/passwd " and change and save the file.
  
GROUPS: 
  
  In compaines, there will be many users in many group, So if we wan to add, delete, user for that particular group use the below commands:
  
            sudo groupadd <groupname>  --> want to add a new group
   
            sudo groupdel <groupname>   --> want to delete the whole group
            
            sudo adduser <username> <groupname> --> want to add a particular user to particular group.
            
            sudo deluser <username> <groupname> --> want to delete a user from the group.
            
PERMISSIONS:

  7 7 7
  
  1st 7 --> Stands for the owner of the files and folders, that can read, write and execute.
  2nd 7 --> Stands for the member of the group that can access to read, write and execute.
  3rd 7 --> Stands for the Everybody else can access in the world.
  
  Mostly the configuration files will be in the 775, in order to give permission for everybody should access we has to change permissions to 777 in order to read,write, execute.
  
            sudo chmod 777 <filename> -R 
            sudo chmod 777 <foldername> -R
            
 If we want to change the ownwer ship for the user of the files or folder use the commands below:
 
            sudo chown -R <username> <filename>
            sudo chown -R <username> <foldername>

If we want to change the ownership for the group , use the below command:

            sudo chgroup -R <groupname> <filename>
            sudo chgroup -R <groupname> <foldername>
  
================================================================================================================================


Network Configurations:

  If we want to change the network configuration make sure that you have to restart the services again, example is shown below.
  
            ifconfig ----> Shows all the IPAddresses
            
            sudo dhclient --> will renueal the IPAddress, or lease the IPADDress for extension to use.
   
   Note: Below commands says our network restart,stop, start
   
            sudo /etc/init.d/networking restart 
            
            sudo /etc/init.d/networking start
            
            sudo /etc/init.d/networking stop
            
   Our Network configuration file will be in the fallowing below directory:
   
            sudo vim /ettc/network/interfaces 
            
     Note: After seeing here in the config file look like this as below.
     
            auto eth0 --> Stands for the First Network card. Auto means speed.
            iface eth0 inet dhcp 
            
       So we can change or edit from dhcp client to static like as fallows:
       
            auto eth0
            iface etch0 inet static
            address 10.1.10.5 # for Example IPAddress
            netmask 255.255.255.0
            network 10.1.10.0 # Example will be same as the Address but not all of them
            Broadcast 10.1.10.255 # Address range
            Gateway 10.1.10.1 # default gateway example
            
            
       Simply save the changes 

DNS Information:

   Want to Know the DNS Information, use the below command:
   
          sudo vim /etc/resolve.conf (SHows the DNS information)
          
  After changing the DNS, we have to change the Restart the services.

HOSTNAME: 

  Want to know the hostname of the server
  
          sudo /bin/hostname
          
          sudo /bin/hostname <new hostname> 
          
          
PING : 

  Can check with IPaddress or with the Domain name. In windows It iterats only for four times, where as in linux it iterates all the time.
  
==========================================================================================================================


FIREWALL UFW: 

Commands for firwall :

        sudo ufw status
        
        sudo ufw default deny
        sudo ufw default allow
        
        sudo ufw enable
        sudo ufw disable
        
 SECURITY GROUPS:
 
        sudo ufw allow <portnumber> 
        sudo ufw deny <portnumber>
        
        sudo ufw delete allow <port number>
        sudo ufw delete deny <prot number>
        
        sudo ufw allow from < IPAddress> --> Can also mention IPaddress.
        sudo ufw deny from <IPAddress> --> Can also delete the IPAddress.
        
        sudo ufw allow from <IP ADDRESS> to < Port Number>
        sudo ufw allow from <IPADDress> to any port <22> 
        
===========================================================================================================================

SSH & FTP:

SSH: Secure shell Environment

  In order to interact with shell, via putty we have install ssh in our server. So use the below command
  
        sudo apt-get install ssh
        
 Note: SSH uses default port 22. In order to run our ufw should be Inactive.
 
 FTP: File transfer protocal
 
  we has to install "vsftpd" because the System users can upload and download files. Lateron we can use any vsftpd client like Filezilla, winscp etc..  and also after installing make sure that we have to enable the config file.
  
  
        sudo apt-get install vsftpd
        
        sudo vim /etc/vsftpd.conf --> enable the local_enable = YES
                                                 write_enable = YES
                                                 
                                                 
        sudo service vsftpd restart 
        
==============================================================================================================================


LINUX BACKUP With TAR and CRON JOBS:

BACKUP:

Below command tells that how we can backup the tar file from and put it into another directory

      sudo tar -cvpzf backup.tar.gz --exclude=/var/www/video /var/www
      
      It tells you the name of the file backup.tar.gz should be keep the copy of that file to /var/www excluding /var/www/video directory.
      
      c --> creates the file
      v --> verbose (whats going on with the file)
      p --> permission 
      z --> compress the tar file
      f --> Allows tar to give a file name
      
RECOVERY:

--> Create a recovery directory first

      mkdir recovery
      
      sudo tar -xvpzf wwwbackup.tar.gz -c /recovery
      
CRON JOBS:

  Simply use the below command to schedule a JOB, that has to run by opening a command with
  
      sudo crontab -e
      
    # You can schedule a Job an Example Job is shown as below, and will be shown like below after opening
    
     min          hour       dom(days)       month      dow(week)           commd
    (0-59)        (0-23)       (1-31)         (1-12)       (0-6)             What we want to install
   
   
   The example is shown below :
   
      *             *           *             *           *         sudo tar -cpzf /backupfolder/minutebackup.tar.gz /var/www/wp-content
      
 Note: what it does it take the backup for every minute, In week there will be little confused like 0- sunday, 1-monday, etc.....
 
 
 
  
    
  
      
     
    
  

 
 
             
             
