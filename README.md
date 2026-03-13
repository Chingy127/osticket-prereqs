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

- Windows 11</b> (25H2)

<h2>List of Prerequisites</h2>

- Microsoft Azure Virtual Machine
- Remote Desktop Connection
- IIS (Internet Information Services)
- PHP and MySQL installation files
- osTicket installation files

<h2>Installation Steps</h2>

<p>
<img src="./images/rdp-connect.png" height="80%" width="80%" alt="Remote Desktop Connection"/>
</p>
<p>
This screenshot shows connecting to the Azure virtual machine using Remote Desktop. 
The public IP address from the Azure VM is entered so the computer in the cloud can be accessed remotely.
</p>
<br />

<p>
<img src="./images/windows-login.png" height="80%" width="80%" alt="Windows Login"/>
</p>
<p>
After connecting through Remote Desktop, the Windows virtual machine login screen appears. 
Logging in gives access to the cloud computer where osTicket will be installed.
</p>
<br />

<p>
<img src="./images/installation-files.png" height="80%" width="80%" alt="osTicket installation files"/>
</p>
<p>
This screenshot shows the osTicket installation files that were downloaded and extracted. 
These files include the database software, PHP, and other components required to run osTicket.
</p>
<br />

<p>
<img src="./images/iis-enable.png" height="80%" width="80%" alt="Enable IIS"/>
</p>
<p>
Internet Information Services (IIS) is enabled in Windows Features. 
IIS is a web server that allows the computer to host and run web applications like osTicket.
</p>
<br />

<p>
<img src="./images/cgi-enable.png" height="80%" width="80%" alt="Enable CGI"/>
</p>
<p>
The CGI feature is enabled inside IIS application development features. 
This allows the web server to process dynamic web content required by osTicket.
</p>
<br />

<p>
<img src="./images/iis-working.png" height="80%" width="80%" alt="IIS test page"/>
</p>
<p>
Opening the browser and navigating to localhost displays the IIS welcome page. 
This confirms the web server is installed and working correctly.
</p>
<br />

<p>
<img src="./images/url-rewrite-install.png" height="80%" width="80%" alt="Installing URL Rewrite"/>
</p>
<p>
The IIS URL Rewrite module is installed from the osTicket setup files. 
This module helps IIS properly handle web requests used by the help desk system.
</p>
<br />

<p>
<img src="./images/create-folder.png" height="80%" width="80%" alt="Create folder in C drive"/>
</p>
<p>
A new folder is created in the Windows C: drive. 
This is where the osTicket website files will be placed so the web server can access them.
</p>
<br />

<p>
<img src="./images/dependency-files.png" height="80%" width="80%" alt="Dependency files"/>
</p>
<p>
This screenshot shows the required installation files such as PHP, MySQL, and PHP Manager. 
These programs are necessary for osTicket to function correctly on the server.
</p>
<br />
