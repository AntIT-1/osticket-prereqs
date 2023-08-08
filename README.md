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
- osTicket installation files
- Heidi SQL


<h2>Installation Steps</h2>
First step is to install and configure a VM (virtual machine) in Azure portal. This is ideal so you don't have to download files onto your PC and risk running into any issues. Create a resource group and name it "osTicket". Once resource group is created, then go ahead and install a virtual machine. Preferrably one with 4 CPUs. 

![image](https://github.com/AntIT-1/osticket-prereqs/assets/141161539/97a48517-927e-4070-aec4-ad3d380ea1f0)


</p>
<p>
Now that the virtual machine has been created, you can now remote log into it by copy and paste the public IP address. Click connect and enter the username and password that were assigned to this VM when created in Azure portal. 
  
  ![image](https://github.com/AntIT-1/osticket-prereqs/assets/141161539/3060fa91-4ce1-46fe-a9dc-ce012e87fa0c)




Once in the VM, install/ enable IIS with CGI and common HTTP feartures as well as IIS management console. This can be found in the control panel/ programs then click "Turn windows features on or off". 
![image](https://github.com/AntIT-1/osticket-prereqs/assets/141161539/0c98230e-9edd-42a4-ade2-6c0fe3295b41)



From the Installation Files, download and install the Rewrite Module (rewrite_amd64_en-US.msi)

Create the directory C:\PHP

From the Installation Files, download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP. Download and install VC_redist.x86.exe.

![image](https://github.com/AntIT-1/osticket-prereqs/assets/141161539/07925acb-9bc4-4708-8cb5-56dc62fa365d)

Open IIS Manager and restart the server. Once inside IIS manager go to Sites->Default->osTicket on the right, click "Browse*.80" from there your default browser should open osTicket webserver.
![image](https://github.com/AntIT-1/osticket-prereqs/assets/141161539/f3123c98-8bc6-4960-9a3d-028fe7f41794)
![image](https://github.com/AntIT-1/osticket-prereqs/assets/141161539/0ea9e50e-ee93-45ec-add0-003397d0b203)


Go to PHP manager to enable the following extensions. 
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
![image](https://github.com/AntIT-1/osticket-prereqs/assets/141161539/e49ba3e8-0bcb-424b-a2d6-ad14f2411e79)

Go back into c:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php rename the file to c:\inetpub\wwwroot\osTicket\include\ost-config.php Assign permissions to ost-config.php Disable inheritance->Removeall New Permissions->Everyone->all

![image](https://github.com/AntIT-1/osticket-prereqs/assets/141161539/99e47b89-90b3-422e-a925-8b04dcebf36e)

Now, the initial setup for osTicket can be started by entering username and email.
![image](https://github.com/AntIT-1/osticket-prereqs/assets/141161539/b071a992-fb5d-4fc2-bf13-a699cd7f3e68)

Setup osticket in the browser MySQL Database: osTicket MySQL Username: root MySQL Password: Password1. This is the final step for installing osTicket. 
![image](https://github.com/AntIT-1/osticket-prereqs/assets/141161539/f409dfd0-f9fd-4634-be6b-34d910ed3bc2)

Once you enter username and password to MySQL database, the intall should be complete. 
![image](https://github.com/AntIT-1/osticket-prereqs/assets/141161539/9ab61c25-eda2-4bc0-ac0c-ee952d7ceaa5)









