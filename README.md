<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com/watch?v=nf560_tzR2Y)

<h2>Step By Step</h2>

![image](https://github.com/user-attachments/assets/0f9eefc6-990e-4017-84c0-dcee1b437800)
![Untitled image (1)](https://github.com/user-attachments/assets/f6337eba-36f7-4dd7-9d37-89c8baadc036)

Installation
1. Download Installation Files:
    * Ensure you have access to the required installation files.
2. Install Internet Information Services (IIS):
    * Open the "Server Manager" in Windows.
    * Select "Add roles and features".
    * Choose "Role-based or feature-based installation".
    * Select the current server.
    * In "Server Roles", check "Web Server (IIS)".
    * Under "Role Services", expand:
        * Web Server -> Common HTTP Features and check "Common HTTP Features".
        * Web Server -> Application Development and check "CGI".
        * Management Tools -> IIS Management Console and check "IIS Management Console".
    * Click "Next" and then "Install".
3. Install PHP Manager for IIS:
    * From the installation files, download and install PHPManagerForIIS_V1.5.0.msi.
4. Install Rewrite Module:
    * From the installation files, download and install rewrite_amd64_en-US.msi.
5. Create PHP Directory:
    * Create the directory C:\PHP.
6. Download and Install PHP:
    * From the installation files, download php-7.3.8-nts-Win32-VC15-x86.zip.
    * Unzip the contents into C:\PHP.
    * If you encounter download issues, try using Google Chrome.
7. Install Visual C++ Redistributable:
    * From the installation files, download and install VC_redist.x86.exe.
8. Install MySQL:
    * From the installation files, download and install mysql-5.5.62-win32.msi.
    * Choose "Typical Setup".
    * After installation, launch the Configuration Wizard.
    * Select "Standard Configuration".
    * Set the root password to Password1.
9. Configure IIS for PHP:
    * Open IIS Manager as an administrator.
    * Register PHP from within IIS.
    * Reload IIS by stopping and starting the server.
10. Install osTicket:
    * From the installation files, download osTicket v1.15.8.
    * Extract and copy the "upload" folder to C:\inetpub\wwwroot.
    * Rename the folder from "upload" to "osTicket".
11. Configure osTicket in IIS:
    * Reload IIS.
    * Go to sites -> Default -> osTicket and click “Browse *:80”.
    * Enable required PHP extensions in PHP Manager:
        * php_imap.dll
        * php_intl.dll
        * php_opcache.dll
    * Refresh the osTicket site.
12. Rename and Set Permissions for Configuration File:
    * Rename C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to ost-config.php.
    * Disable inheritance and remove all permissions, then grant "Everyone" full control.
13. Complete osTicket Setup in Browser:
    * Open the osTicket setup page in your browser.
    * Follow the setup instructions, providing the necessary details:
        * Name: Helpdesk
        * Default email: Your chosen email address
    * Set up the MySQL database:
        * Database: osTicket
        * Username: root
        * Password: Password1
    * Click "Install Now!".
14. Clean Up:
    * Delete C:\inetpub\wwwroot\osTicket\setup.
    * Set C:\inetpub\wwwroot\osTicket\include\ost-config.php to read-only.

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

