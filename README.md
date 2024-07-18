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

![Screenshot (2)](https://github.com/user-attachments/assets/353573c9-3b5d-4459-8de8-f8346108cab6)

 
To set up your virtual machine on Microsoft Azure, start by creating a resource group (RG) and naming it. Then, use the Azure portal to search for "Virtual Machine (VM)" and begin creating your VM. Choose your resource group, VM name, region, operating system, and VM size (VCPU). Create a username and strong password for accessing the VM. Double-check all settings, click "Review + Create", verify your configuration, and then click "Create" to deploy your VM. Azure will start setting up your VM based on your specifications.
</p>
<br />

![Screenshot (3)](https://github.com/user-attachments/assets/fe75be67-21b4-44b5-bb30-d14f43a362a4)


After completing the initial setup steps, the next phase involves downloading essential files to fully configure OSticket. Begin by downloading and installing IIS. Once installed, open it and enable the following features: CGI, Common HTTP Features, Internet Information Services, Web Management Tools, and IIS Management Console. Next, return to the downloaded files and install PHP Manager for IIS and the Rewrite Module. Proceed by creating a directory at C:\PHP. Subsequently, revisit the downloaded files to obtain PHP 7.3.8 and extract its contents into the C:\PHP directory. Ensure to retain all files when prompted during the download process.
</p>
<br />

![Screenshot (4)](https://github.com/user-attachments/assets/58fca7d3-4853-47f3-95a2-010e46533339)

Now you will install VC_redist.x86.exe from the Installation Files folder. Then, proceed to install MySQL 5.5.62. Choose the Typical Setup option during installation and, after installation completes, launch the Configuration Wizard. Opt for Standard Configuration and set the root password to "Password1". Next, open Internet Information Services (IIS) as an Administrator and register PHP within IIS. To ensure the changes take effect, reload IIS by stopping and starting the server through the IIS management console. Now, it's time to install osTicket v1.15.8. Download the osTicket package from the Installation Files folder, extract the contents, and locate the "upload" folder. Copy this folder to c:\inetpub\wwwroot. Within c:\inetpub\wwwroot, rename the "upload" folder to "osTicket".Lastly, reload IIS once more by stopping and starting the server to finalize the setup. Following these steps will successfully configure osTicket v1.15.8 on your system, ensuring everything is set up correctly for use.
</p>
<br />

![Screenshot (5)](https://github.com/user-attachments/assets/2a4c9185-1150-4a8e-8f57-f345de787a9f)

First, in Internet Information Services (IIS), locate "osTicket" under sites -> Default. Click "Browse *:80". Now double click PHP Manager in IIS and click “Enable or disable an extension”to enable php_imap.dll, php_intl.dll, and php_opcache.dll, then refresh your browser to apply changes. Next, rename ost-config.php from C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to ost-config.php. Adjust its permissions by removing existing ones, disabling inheritance, and granting full access to Everyone. Continue setting up osTicket in your browser by naming your helpdesk and configuring the default email for customer inquiries. Download and install HeidiSQL from the provided Installation Files. Open HeidiSQL, create a new session using root for the username and Password1 for the password. Connect to this session and create a database named "osTicket." Return to your browser setup, enter osTicket for MySQL Database, root for MySQL Username, Password1 for MySQL Password, and click "Install Now!" Once installation completes, access your help desk login page at http://localhost/osTicket/scp/login.php. For end users, direct them to http://localhost/osTicket/. Finally, clean up by deleting C:\inetpub\wwwroot\osTicket\setup and setting C:\inetpub\wwwroot\osTicket\include\ost-config.php to read-only permissions.
</p>
<br />
