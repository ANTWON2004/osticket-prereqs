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

- Computer 
- Virtual Machine
- Remote Desktop
- Mircosoft Azure
- Internet Information Services

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To set up your virtual machine on Microsoft Azure, start by creating a resource group (RG) and naming it. Then, use the Azure portal to search for "Virtual Machine (VM)" and begin creating your VM. Choose your resource group, VM name, region, operating system, and VM size (VCPU). Create a username and strong password for accessing the VM. Double-check all settings, click "Review + Create", verify your configuration, and then click "Create" to deploy your VM. Azure will start setting up your VM based on your specifications.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After completing the initial setup steps, the next phase involves downloading essential files to fully configure OSticket. Begin by downloading and installing IIS. Once installed, open it and enable the following features: CGI, Common HTTP Features, Internet Information Services, Web Management Tools, and IIS Management Console. Next, return to the downloaded files and install PHP Manager for IIS and the Rewrite Module. Proceed by creating a directory at C:\PHP. Subsequently, revisit the downloaded files to obtain PHP 7.3.8 and extract its contents into the C:\PHP directory. Ensure to retain all files when prompted during the download process.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now you will install VC_redist.x86.exe from the Installation Files folder. Then, proceed to install MySQL 5.5.62. Choose the Typical Setup option during installation and, after installation completes, launch the Configuration Wizard. Opt for Standard Configuration and set the root password to "Password1". Next, open Internet Information Services (IIS) as an Administrator and register PHP within IIS. To ensure the changes take effect, reload IIS by stopping and starting the server through the IIS management console. Now, it's time to install osTicket v1.15.8. Download the osTicket package from the Installation Files folder, extract the contents, and locate the "upload" folder. Copy this folder to c:\inetpub\wwwroot. Within c:\inetpub\wwwroot, rename the "upload" folder to "osTicket".Lastly, reload IIS once more by stopping and starting the server to finalize the setup. Following these steps will successfully configure osTicket v1.15.8 on your system, ensuring everything is set up correctly for use.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
