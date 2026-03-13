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

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 46 00 PM" src="https://github.com/user-attachments/assets/b93d495d-cc11-49c6-a94e-57b59cd696ce" />
</p>
<p>
The osTicket compressed file is extracted. 
This step prepares the osTicket website files so they can be placed on the web server.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 49 02 PM" src="https://github.com/user-attachments/assets/948bf373-6ec8-40a4-8bd3-d1ae0e33e7a6" />
</p>
<p>
The "upload" folder from the osTicket installation files is copied into the IIS web server directory located at C:\inetpub\wwwroot. 
This allows IIS to host the osTicket website.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 52 03 PM" src="https://github.com/user-attachments/assets/97e03bac-3cda-4b82-baa8-0bf2bb0bf0cd" />
</p>
<p>
Inside IIS Manager, the osTicket folder appears under the Default Web Site. 
This confirms the website files were successfully added to the web server.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 58 29 PM" src="https://github.com/user-attachments/assets/bbed7501-9421-49ba-b84e-19541e9b2f70" />
</p>
<p>
PHP extensions are enabled inside IIS. 
These extensions provide additional functionality required for osTicket to run properly.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 2 00 58 PM" src="https://github.com/user-attachments/assets/4f2e041a-484f-465d-9622-ba431a85b4b1" />
</p>
<p>
The osTicket configuration file named "ost-config.php" is located inside the include folder. 
This file stores important configuration settings for the help desk system.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 2 03 36 PM" src="https://github.com/user-attachments/assets/3b3420bf-60bc-4113-9b31-f33a17a3f59e" />
</p>
<p>
Permissions are updated for the configuration file so the web server can modify it during installation. 
This allows osTicket to save database settings and complete the setup process.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 2 08 22 PM" src="https://github.com/user-attachments/assets/4abcd470-218c-4149-9113-2417bc52f864" />
</p>
<p>
The osTicket installation page is opened in the browser. 
Basic system information such as the help desk name, admin user, and email address are entered to complete the setup.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 2 10 39 PM" src="https://github.com/user-attachments/assets/141c440f-d7af-48d0-93c1-1b9dbe23e07d" />
</p>
<p>
HeidiSQL is installed to help manage the MySQL database used by osTicket. 
This tool makes it easier to view and manage the database tables.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 2 12 39 PM" src="https://github.com/user-attachments/assets/21a63213-b403-4aae-bbce-6876ffbe6d3b" />
</p>
<p>
HeidiSQL successfully connects to the MySQL server running on the machine. 
This confirms the database service is running and accessible.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 2 15 17 PM" src="https://github.com/user-attachments/assets/069d70ab-40be-476d-9aea-2e7f9276fa82" />
</p>
<p>
The installation completes successfully. 
This screen confirms that the osTicket help desk system has been installed and is ready to use.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 2 19 43 PM" src="https://github.com/user-attachments/assets/672ea62d-369a-41bf-821e-0e8197422f17" />
</p>
<p>
The osTicket admin login page is opened. 
Administrators use this page to sign in and manage support tickets within the help desk system.
</p>
<br />

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-07 at 2 25 25 PM" src="https://github.com/user-attachments/assets/a0035c7b-779a-462a-9cbd-5fcfd585474f" />

</p>
<p>
After logging in, the osTicket dashboard is displayed. 
This dashboard allows administrators to view, manage, and respond to support tickets submitted by users.
</p>
<br />
