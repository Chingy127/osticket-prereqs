<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>


<h1>osTicket - Prerequisites and Installation</h1>

Now that the Azure Virtual Machine has been created and you have successfully logged into it through Remote Desktop, the next step is to install the required components for **osTicket**, an open-source help desk ticketing system.

This section walks through downloading the required installation files and configuring the server environment needed to run osTicket.

---

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines / Compute)
- Remote Desktop
- Internet Information Services (IIS)

---

<h2>Operating Systems Used</h2>

- Windows 11 (Azure Virtual Machine)

---

<h2>Required Installation Files</h2>

Download the required osTicket installation package before starting the setup.

Download here:

https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD

Place the file on the **Desktop of the Virtual Machine** and extract it before continuing.

---

<h2>Installation Walkthrough</h2>

---

<h3>Step 1 – Connect to the Azure Virtual Machine</h3>

<p>
<img width="1162" height="705" alt="Screenshot 2026-03-06 at 1 08 09 PM" src="https://github.com/user-attachments/assets/076976c6-231d-419e-a5b9-a85c2e6ae45b" />
</p>

Open **Remote Desktop** on your computer.

Enter the **Public IP Address** of the Azure Virtual Machine that was created earlier.

Click **Connect** to remotely access the virtual machine.

---

<h3>Step 2 – Log Into the Virtual Machine</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 10 49 PM" src="https://github.com/user-attachments/assets/aad84666-2e80-4a4e-a0df-0d14f6ee0e80" />
</p>

When the Windows login screen appears, enter the **username and password** created when configuring the Azure Virtual Machine.

After logging in, you will have full access to the Windows environment where osTicket will be installed.

---

<h3>Step 3 – Locate the osTicket Installation Files</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 15 50 PM" src="https://github.com/user-attachments/assets/6dc4f8d3-925c-4927-b23c-9e129df0b31d" />
</p>

Locate the **osTicket Installation Files** folder that was downloaded earlier.

Right-click the compressed file and select **Extract All**.

After extracting the files, open the folder to view the installation components that will be used throughout the setup process.

---

<h3>Step 4 – Enable Internet Information Services (IIS)</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 20 10 PM" src="https://github.com/user-attachments/assets/d9970458-f1eb-4a4e-b172-d3b246a1b4ff" />
</p>

Open the **Windows Start Menu** and search for:

Windows Features

Select **Turn Windows features on or off**.

Enable the following feature:

Internet Information Services (IIS)

IIS acts as the web server that will host the osTicket help desk application.

Click **OK** to install the feature.

---

<h3>Step 5 – Enable CGI for IIS</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 21 01 PM" src="https://github.com/user-attachments/assets/15b170f8-b366-4334-a01a-34a3d6ec26e2" />
</p>

Inside the **Internet Information Services** section, expand:

World Wide Web Services → Application Development Features

Enable the following option:

CGI

The CGI module allows IIS to process dynamic web content required by PHP applications like osTicket.

Click **OK** to finish installing the feature.

---

<h3>Step 6 – Verify IIS is Working</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 23 30 PM" src="https://github.com/user-attachments/assets/89fca8d9-52a9-4b23-ae1c-bd5bd383cadd" />
</p>

Open **Microsoft Edge** inside the Virtual Machine.

In the address bar type:

localhost

Press **Enter**.

If IIS is installed correctly, the **IIS Welcome Page** will appear. This confirms the web server is running properly.

---

<h3>Step 7 – Install the IIS URL Rewrite Module</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 29 36 PM" src="https://github.com/user-attachments/assets/51fe0d38-0132-4809-96d4-09d5e8fce052" />
</p>

Locate the **URL Rewrite installer** inside the extracted osTicket installation files.

Double-click the installer and follow the prompts to install it.

This module allows IIS to correctly process and route web requests used by osTicket.

---

<h3>Step 8 – Create a Directory for PHP</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 31 03 PM" src="https://github.com/user-attachments/assets/f3a9ed50-f2d5-4aec-b141-0b76ca2ea8fe" />
</p>

Open **File Explorer**.

Navigate to the **C:\ drive**.

Create a new folder named:

PHP

This directory will store the PHP runtime files used by the web server.

---

<h3>Step 9 – Locate the PHP Installation Files</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 32 39 PM" src="https://github.com/user-attachments/assets/e0a79c21-cc07-4688-bcd2-d316ce0a4b2b" />
</p>

Open the **osTicket installation files folder**.

Locate the compressed **PHP installation package** included in the download.

These files contain the PHP runtime required to run the osTicket application.

---

<h3>Step 10 – Extract PHP to the C:\PHP Folder</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 32 47 PM" src="https://github.com/user-attachments/assets/d0875faf-3726-4dff-bdb0-4ba9a508efb4" />
</p>

Right-click the PHP compressed file and select **Extract All**.

Extract the contents into the folder created earlier:

C:\PHP

This makes the PHP runtime accessible to the IIS web server.

---

<h3>Step 11 – Install Microsoft Visual C++ Redistributable</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 35 29 PM" src="https://github.com/user-attachments/assets/7a5d21b4-f44c-4381-b4b2-ac3909616c6c" />
</p>

Locate the **Microsoft Visual C++ Redistributable installer** inside the setup files.

Run the installer and complete the setup.

This software provides system components required for several dependencies used by PHP and osTicket.

---

<h3>Step 12 – Install MySQL Server</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 36 04 PM" src="https://github.com/user-attachments/assets/406bc37f-24f3-442e-b245-2e11308c2a55" />
</p>

Locate the **MySQL installer** inside the setup files.

Launch the **MySQL Setup Wizard** and follow the prompts to install the database server.

MySQL will store the help desk ticket data used by osTicket.

---

<h3>Step 13 – Open Internet Information Services (IIS) Manager</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 41 35 PM" src="https://github.com/user-attachments/assets/1bb9b2c0-99ad-4cb2-91aa-96489e2bbaf7" />
</p>

Open the **Windows Search Bar** inside the Virtual Machine.

Search for:

Internet Information Services (IIS) Manager

Click the application to launch the IIS management console.

This tool is used to configure the web server that will host osTicket.

---

<h3>Step 14 – Open IIS Manager</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 42 22 PM" src="https://github.com/user-attachments/assets/e70043bf-6a2c-4d62-8a13-dbe655f97da7" />
</p>

When IIS Manager opens, you will see the **server name** on the left side panel.

Expand the server to view the available configuration tools and web server settings.

This interface will be used to connect PHP with IIS and configure the osTicket website.

---

<h3>Step 15 – Configure PHP Manager</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 43 31 PM" src="https://github.com/user-attachments/assets/32cd43f3-f707-4945-8cd7-39b52edf8476" />
</p>

Inside IIS Manager, locate and open **PHP Manager**.

Click the option to **Register a new PHP version**.

Navigate to the folder:

C:\PHP

Select the file:

php-cgi.exe

This connects PHP to IIS so the server can run PHP applications like osTicket.

---

<h3>Step 16 – Extract the osTicket Files</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 46 00 PM" src="https://github.com/user-attachments/assets/b93d495d-cc11-49c6-a94e-57b59cd696ce" />
</p>

Locate the **osTicket compressed file** inside the installation folder.

Right-click the file and select **Extract All**.

This will create a folder containing the osTicket website files.

---

<h3>Step 17 – Move osTicket Files to the Web Server Directory</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 49 02 PM" src="https://github.com/user-attachments/assets/948bf373-6ec8-40a4-8bd3-d1ae0e33e7a6" />
</p>

Open the extracted osTicket folder.

Locate the folder named:

upload

Copy the **upload folder** and paste it into the IIS web server directory:

C:\inetpub\wwwroot

After copying, rename the folder from **upload** to:

osTicket

This allows IIS to host the osTicket website.

---

<h3>Step 18 – Verify the osTicket Website Appears in IIS</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 52 03 PM" src="https://github.com/user-attachments/assets/97e03bac-3cda-4b82-baa8-0bf2bb0bf0cd" />
</p>

Return to **IIS Manager**.

Expand:

Default Web Site

You should now see the **osTicket folder** listed under the web server.

This confirms that the website files were successfully placed in the correct directory.

---

<h3>Step 19 – Enable Required PHP Extensions</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 1 58 29 PM" src="https://github.com/user-attachments/assets/bbed7501-9421-49ba-b84e-19541e9b2f70" />
</p>

Inside IIS Manager, open **PHP Manager**.

Click **Enable or Disable an Extension**.

Enable the required PHP extensions needed by osTicket.

These extensions allow the help desk system to interact with the database and process dynamic content.

---

<h3>Step 20 – Locate the osTicket Configuration File</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 2 00 58 PM" src="https://github.com/user-attachments/assets/4f2e041a-484f-465d-9622-ba431a85b4b1" />
</p>

Open File Explorer and navigate to:

C:\inetpub\wwwroot\osTicket\include

Locate the file:

ost-config.php

This file stores configuration settings used by the osTicket system.

---

<h3>Step 21 – Update File Permissions</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 2 03 36 PM" src="https://github.com/user-attachments/assets/3b3420bf-60bc-4113-9b31-f33a17a3f59e" />
</p>

Right-click the **ost-config.php** file and open **Properties**.

Modify the file permissions so the web server can update the file during installation.

This allows osTicket to store database configuration settings.

---

<h3>Step 22 – Start the osTicket Web Installer</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 2 08 22 PM" src="https://github.com/user-attachments/assets/4abcd470-218c-4149-9113-2417bc52f864" />
</p>

Open a web browser inside the Virtual Machine.

Navigate to:

http://localhost/osTicket

The osTicket setup page will appear.

Enter the required information such as:

- Helpdesk Name  
- Default Email Address  
- Admin Username  
- Admin Password

Continue through the installation wizard.

---

<h3>Step 23 – Install HeidiSQL</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 2 10 39 PM" src="https://github.com/user-attachments/assets/141c440f-d7af-48d0-93c1-1b9dbe23e07d" />
</p>

Install **HeidiSQL** using the installer included in the setup files.

HeidiSQL is a database management tool used to view and manage the MySQL database used by osTicket.

---

<h3>Step 24 – Connect to the MySQL Database</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 2 12 39 PM" src="https://github.com/user-attachments/assets/21a63213-b403-4aae-bbce-6876ffbe6d3b" />
</p>

Open **HeidiSQL**.

Create a new session and connect to the **MySQL server running on localhost**.

Successful connection confirms the database service is working properly.

---

<h3>Step 25 – Complete the osTicket Installation</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 2 15 17 PM" src="https://github.com/user-attachments/assets/069d70ab-40be-476d-9aea-2e7f9276fa82" />
</p>

After completing the setup wizard, osTicket will display a confirmation page indicating the installation was successful.

This means the help desk system is now fully installed.

---

<h3>Step 26 – Access the Admin Login Page</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-06 at 2 19 43 PM" src="https://github.com/user-attachments/assets/672ea62d-369a-41bf-821e-0e8197422f17" />
</p>

Open the osTicket admin login page in your browser.

Enter the **administrator credentials** created during installation.

Administrators use this portal to manage tickets and configure the help desk system.

---

<h3>Step 27 – View the osTicket Dashboard</h3>

<p>
<img width="1440" height="900" alt="Screenshot 2026-03-07 at 2 25 25 PM" src="https://github.com/user-attachments/assets/a0035c7b-779a-462a-9cbd-5fcfd585474f" />
</p>

After logging in, the **osTicket Dashboard** will appear.

From this dashboard administrators can:

- View incoming support tickets
- Assign tickets to support agents
- Manage users and departments
- Monitor help desk activity

The osTicket help desk system is now fully operational.
