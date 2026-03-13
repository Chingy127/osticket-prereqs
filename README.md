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
<img width="1162" height="705" alt="Screenshot 2026-03-06 at 1 08 09 PM" src="https://github.com/user-attachments/assets/076976c6-231d-419e-a5b9-a85c2e6ae45b" />
</p>
<p>
This screenshot shows connecting to the Azure virtual machine using Remote Desktop. 
The public IP address from the Azure VM is entered so the computer in the cloud can be accessed remotely.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 10 49 PM" src="https://github.com/user-attachments/assets/aad84666-2e80-4a4e-a0df-0d14f6ee0e80" />
</p>
<p>
After connecting through Remote Desktop, the Windows virtual machine login screen appears. 
Logging in gives access to the cloud computer where osTicket will be installed.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 15 50 PM" src="https://github.com/user-attachments/assets/6dc4f8d3-925c-4927-b23c-9e129df0b31d" />
</p>
<p>
This screenshot shows the osTicket installation files that were downloaded and extracted. 
These files include the database software, PHP, and other components required to run osTicket.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 20 10 PM" src="https://github.com/user-attachments/assets/d9970458-f1eb-4a4e-b172-d3b246a1b4ff" />
</p>
<p>
Internet Information Services (IIS) is enabled in Windows Features. 
IIS is a web server that allows the computer to host and run web applications like osTicket.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 21 01 PM" src="https://github.com/user-attachments/assets/15b170f8-b366-4334-a01a-34a3d6ec26e2" />
</p>
<p>
The CGI feature is enabled inside IIS application development features. 
This allows the web server to process dynamic web content required by osTicket.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 23 30 PM" src="https://github.com/user-attachments/assets/89fca8d9-52a9-4b23-ae1c-bd5bd383cadd" />
</p>
<p>
Opening the browser and navigating to localhost displays the IIS welcome page. 
This confirms the web server is installed and working correctly.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 29 36 PM" src="https://github.com/user-attachments/assets/51fe0d38-0132-4809-96d4-09d5e8fce052" />
</p>
<p>
The IIS URL Rewrite module is installed from the osTicket setup files. 
This module helps IIS properly handle web requests used by the help desk system.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 31 03 PM" src="https://github.com/user-attachments/assets/f3a9ed50-f2d5-4aec-b141-0b76ca2ea8fe" />
</p>
<p>
A new folder is created in the Windows C: drive. 
This is where the osTicket website files will be placed so the web server can access them.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 32 39 PM" src="https://github.com/user-attachments/assets/e0a79c21-cc07-4688-bcd2-d316ce0a4b2b" />

</p>
<p>
This screenshot shows the required installation files such as PHP, MySQL, and PHP Manager. 
These programs are necessary for osTicket to function correctly on the server.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 32 47 PM" src="https://github.com/user-attachments/assets/d0875faf-3726-4dff-bdb0-4ba9a508efb4" />
</p>
<p>
This screenshot shows the contents of the PHP folder after extracting the PHP installation files. 
These files allow the web server to run PHP applications, which osTicket requires to function.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 33 58 PM" src="https://github.com/user-attachments/assets/d410d76a-209d-486c-9fcc-08d831f91682" />
</p>
<p>
The PHP compressed file is extracted to the C:\PHP directory. 
This places the PHP files in a location where the web server can access them.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 35 29 PM" src="https://github.com/user-attachments/assets/7a5d21b4-f44c-4381-b4b2-ac3909616c6c" />
</p>
<p>
Microsoft Visual C++ Redistributable is installed. 
This software provides system components required for some of the osTicket dependencies to run properly.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 36 04 PM" src="https://github.com/user-attachments/assets/406bc37f-24f3-442e-b245-2e11308c2a55" />
<p>
The MySQL setup wizard is launched. 
MySQL will be used as the database that stores ticket information for the help desk system.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 41 35 PM" src="https://github.com/user-attachments/assets/1bb9b2c0-99ad-4cb2-91aa-96489e2bbaf7" />
</p>
<p>
The Windows search bar is used to locate Internet Information Services (IIS) Manager. 
This tool is used to configure and manage the web server.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 42 22 PM" src="https://github.com/user-attachments/assets/e70043bf-6a2c-4d62-8a13-dbe655f97da7" />
</p>
<p>
IIS Manager is opened to view and manage the web server settings. 
From here, features such as PHP Manager and URL Rewrite can be configured.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 43 31 PM" src="https://github.com/user-attachments/assets/32cd43f3-f707-4945-8cd7-39b52edf8476" />
</p>
<p>
PHP Manager is configured by selecting the php-cgi executable file. 
This connects PHP with the IIS web server so PHP applications like osTicket can run correctly.
</p>
<br />
