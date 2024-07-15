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

(11) Register PHP manager
Click PHP Manager -> select register new PHP version -> provide "C:\PHP\php-cgi.exe" 

(12) Restart IIS server.
