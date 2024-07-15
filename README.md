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

- IIS
- PHP Manager
- Rewrite Module
- VC_redistx86
- MySQL 5.5.62
- Heidi SQL

<h2>Installation Steps</h2>

(1) Create a virtual machine (VM) in Azure. Select Windows 10 for image (base operating system).
![image alt](https://github.com/JordanJefferson/osticket-prereqs/blob/258a9d8a8055508aae069cdf51bd3bdf5271a6f0/Capture.PNG)


(2) Copy your virtual machines public ip and paste it into remote desktop.  Then login using the credentials you created when you made the VM.

![image alt](https://github.com/JordanJefferson/osticket-prereqs/blob/1f7b4339eeac1fc197344d0ef39225b333ebc45a/Capture.PNG2.PNG)


(3) Once the VM is open, install/enable IIS. Open Control Panel -> Programs -> Turn Windows features on or off.
Enable/expand the following 

![image alt](https://github.com/JordanJefferson/osticket-prereqs/blob/18137d739749e9992bd465c4819048d25d465aa8/Capture.PNG3.PNG)
Click OK to confirm changes.

