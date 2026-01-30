<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>


<h2>Project Overview</h2>
This project demonstrates the installation and initial setup of an enterprise-style ticketing system (osTicket) on a Windows-based environment using IIS, PHP, and MySQL. The focus is on prerequisites, dependencies, and successful deployment.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- PHP
- MySQL
- osTicket
- HeidiSQL

<h2>Operating Systems Used </h2>

- Windows 10 Enterprise, version 22H2 - x64 Gen2

<h2>List of Prerequisites</h2>

- IIS enabled with CGI support.
- PHP registered with IIS via PHP Manager.
- IIS URL Rewrite Module installed.
- Visual C++ Redistributable (x86) installed.
- PHP extensions enabled: (php_imap.dll, php_intl.dll, php_opcache.dll)
- MySQL server configured and accessible.

<h2>Installation Steps</h2>

<p>
<img src="screenshots/step1-azure-vm-rdp.png.png" width="960" />
</p>
<p>
1) Connect to a Windows virtual machine using Remote Desktop(In this case, I used an Azure virtual machine). Once inside the VM, <a href="https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD" target="_blank" rel="noopener noreferrer">
  Download osTicket Installation Files
</a>
</p>
<br />

<p>
<img src="screenshots/Screenshot from 2026-01-16 10-35-40.png" width="960" />
</p>
<p>
2) Extract the contents to the desktop. After extracting the archive, confirm that a folder named osTicket-Installation-Files is present. This folder will be used throughout the setup process to install osTicket and its required dependencies.
</p>
<br />

<p>
<img src="screenshots/Screenshot from 2026-01-16 10-40-20.png" width="960" />
</p>
<p>
3) Open Windows Features on the virtual machine and enable Internet Information Services (IIS). Within the IIS feature set, navigate to World Wide Web Services → Application Development Features and make sure CGI is checked. Apply the changes and allow Windows to install the required components before proceeding.
</p>
<br />

<p>
<img src="screenshots/Screenshot from 2026-01-16 10-45-51.png" width="960" />
</p>
<p>
4) From the osTicket-Installation-Files folder, locate and run PHPManagerForIIS_V1.5.0.msi to install PHP Manager for IIS. Complete the installation using the default settings.
</p>
<br />

<p>
<img src="screenshots/Screenshot from 2026-01-16 10-46-46.png" width="960" />
</p>
<p>
5) From the osTicket-Installation-Files folder, locate and run rewrite_amd64_en-US.msi to install the IIS URL Rewrite Module. Complete the installation using the default options.
</p>
<br />

<p>
<img src="screenshots/Screenshot from 2026-01-16 10-49-51.png" width="960" />
</p>
<p>
6) Create a new directory at C:\PHP on the virtual machine.
</p>
<br />

<p>
<img src="screenshots/Screenshot from 2026-01-16 10-51-01.png" width="960" />
</p>
<p>
7) From the osTicket-Installation-Files folder, extract php-7.3.8-nts-Win32-VC15-x86.zip directly into the C:\PHP directory created in the previous step. After extraction, verify that the PHP files are present inside the C:\PHP folder.
</p>
<br />

<p>
<img src="screenshots/Screenshot from 2026-01-16 10-52-23.png" width="960" />
</p>
<p>
8) From the osTicket-Installation-Files folder, run VC_redist.x86.exe to install the Microsoft Visual C++ Redistributable package. Complete the installation using the default settings before continuing to the next step.
</p>
<br />

<p>
<img src="screenshots/Screenshot from 2026-01-16 10-53-56.png" width="960" />
</p>
<p>
9) From the osTicket-Installation-Files folder, run mysql-5.5.62-win32.msi to begin installing MySQL Server. When prompted during the setup, select a Typical installation and allow the installer to complete.
</p>
<br />

<p>
<img src="screenshots/Screenshot from 2026-01-16 10-55-02.png" width="960" />
</p>
<p>
10) After the MySQL installation finishes, launch the MySQL Configuration Wizard. Select Standard Configuration to proceed with the default server settings.
</p>
<br />

<p>
<img src="screenshots/Screenshot from 2026-01-16 10-57-15.png" width="960" />
</p>
<p>
11) During the configuration process, set a simple password for the MySQL root user that you can easily remember.
</p>
<br />
