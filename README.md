<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- IIS
- PHP Manager
- Rewrite Module
- VC_redistx86
- MySQL 5.5.62
- Heidi SQL
- osTicket v1.15.8

<h2>Installation Steps</h2>

(1) Create a virtual machine (VM) in Azure. Select Windows 10 for image (base operating system).
![image alt](https://github.com/JordanJefferson/osticket-prereqs/blob/258a9d8a8055508aae069cdf51bd3bdf5271a6f0/Capture.PNG) 


(2) Copy your virtual machines public ip and paste it into remote desktop.  Then login using the credentials you created when you made the VM.

![image alt](https://github.com/JordanJefferson/osticket-prereqs/blob/1f7b4339eeac1fc197344d0ef39225b333ebc45a/Capture.PNG2.PNG)


(3) Once the VM is open, install/enable IIS. Open Control Panel -> Programs -> Turn Windows features on or off.
Enable/expand the following 

![image alt](https://github.com/JordanJefferson/osticket-prereqs/blob/18137d739749e9992bd465c4819048d25d465aa8/Capture.PNG3.PNG)
Click OK to confirm changes.


(4) Download and install PHP Manager. https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view?usp=share_link  

(5) Download and install the Rewrite Module.  https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=share_link

(6) Create a directory. Open File Explorer -> This PC -> Windows (C:) -> create new folder named PHP

(7) Download and intall PHP.  Then extract the contents into C:PHP folder.  https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=share_link

(8) Download and install VC_redist.x86.exe.  https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=share_link

(9) download and instal MySQL.  Choose Typical setup type -> Launch Configuration Wizard after install -> Standard configuration -> Install As Windows Service.  https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view?usp=share_link

(10) Open IIS as Administator.  
Type IIS in Windows search bar, click Run as Administrator

(11) Register PHP manager.  
Click PHP Manager -> select register new PHP version -> provide "C:\PHP\php-cgi.exe" 

(12) Restart IIS server.  
![image alt](https://github.com/JordanJefferson/osticket-prereqs/blob/b84b56feada1ff52a2d416d4a3e3bcf94a13d46e/Capture.PNG4.PNG)


(13) Download and install osTicket-v1.15.8.zip  https://drive.google.com/file/d/1VeVXKlzHDRjeaVUL99ptq7qYbrbXdFxJ/view?usp=drive_link
open 2 file explorers  
in 1 go to downloads -> osTicket-v1.15.8  
in 2 go to C: -> inetpub -> wwwroot  
Drag "upload" from first file to the second  
Within C:\inetpub\wwwroot, rename "upload" to "osTicket"

(14) Restart the IIS again

(15) Open osTicket  
Click Sites -> Default Web Site -> osTicket (red) -> Browse *:80 (http) (blue)  
![image alt](https://github.com/JordanJefferson/osticket-prereqs/blob/db86348c581780c026d34c81db6d0f0d228868b5/Capture.PNG%205.PNG)  

osTicket Should open in a different web browser  
![image alt](https://github.com/JordanJefferson/osticket-prereqs/blob/a1b649b890d9905f81a38f00a36123cbb39e4935/Capture.PNG6.PNG)  

(16) Enable Extensions  
Open IIS -> PHP Manager -> Select "Enable or disable Extension  
Enable PHP_imap.dll, PHP_intl.dll, and PHP_opcache.dll  

(17) Refresh osTicket   
APCu Extension and Zend OPcache Extension should be the only ones with a red (X)  
![image alt](https://github.com/JordanJefferson/osticket-prereqs/blob/b630e41181308f4c5c54424cb6f40f63efe2e2de/Capture.PNG7.PNG)   

(18) Rename ost-config.php   
open file explorer -> go to C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php  
rename it to ost-config.php

(19) Assign Permissions ost-config.php
right click ost-config.php -> properties -> security -> advanced -> Disable inheritance -> Remove All
Inherited Permissions   
Add -> select a principal -> type "everyone" as the object name -> click "OK" -> select "Full Control" -> OK -> Apply -> OK   

(20) Continue Setting up osTicket 
fill out "System Settings" and "Admin User" portion  
![image alt](https://github.com/JordanJefferson/osticket-prereqs/blob/33e012b7b597c88be9bd120e7c0173e29f25e566/Capture.PNG8.PNG)   

(21) Download and install HeidiSQL https://docs.google.com/document/d/1WovrX2DaS9xkfaSr4LXyB4YnnWpXIgPCMMbbfgHmGVw/edit  
Open HeidiSQL and use the login credentials you made with "mySQL"  

(22) Create new database  
right click on "Unnamed" and create a new database called "osTicket"  

(23) Finish osTicket installation  
Go back to osTicket browser and fill out "Database Settings" portion
