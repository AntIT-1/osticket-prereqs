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



<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
