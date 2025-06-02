<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>
<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites, installation, and configuration of the open-source help desk ticketing system osTicket, as well as testing with mock users to demonstrate functionality. This project was completed as part of the CourseCareers IT course to build hands-on experience with IT infrastructure and ticketing systems.
<h2>Environments and Technologies Used</h2>
Microsoft Azure (Virtual Machines/Compute)

Remote Desktop

Internet Information Services (IIS)

PHP

MySQL

osTicket

<h2>Operating Systems Used</h2>
Windows 11 (21H2)

Windows Server 2022

<h2>List of Prerequisites</h2>
Microsoft Azure Account: A subscription to create and manage a Windows Server 2022 virtual machine.

Windows Server 2022 VM: A virtual machine provisioned in Azure with Remote Desktop enabled.

PHP 7.4 or higher: Required to run osTicket, installed on the Windows Server.

MySQL 5.7 or higher: Database backend for osTicket to store ticket data.

IIS with CGI Module: Configured to host the osTicket web application.

osTicket Installation Files: Downloaded from the official osTicket website (e.g., version 1.17 or latest stable release).

PHP Manager for IIS: To manage PHP settings within IIS.

MySQL Workbench (optional): For easier database management and configuration.

Web Browser: For accessing the osTicket web interface and testing.

<h2>Installation Steps</h2>
<p>
<img src="https://i.imgur.com/YOUR_SCREENSHOT_1.png" height="80%" width="80%" alt="Creating Azure VM"/>
</p>
<p>
<b>Step 1: Set Up Azure Virtual Machine</b><br />
- Log in to the Microsoft Azure portal and create a Windows Server 2022 virtual machine.
- Configure the VM with at least 2 vCPUs and 4GB RAM to ensure smooth performance.
- Enable Remote Desktop Protocol (RDP) and note the public IP address for remote access.
- Use Remote Desktop to connect to the VM with the provided credentials.
</p>
<br />
<p>
<img src="https://i.imgur.com/YOUR_SCREENSHOT_2.png" height="80%" width="80%" alt="Configuring IIS and PHP"/>
</p>
<p>
<b>Step 2: Install and Configure IIS and PHP</b><br />
- On the Windows Server, open Server Manager and add the IIS role with the CGI module enabled.
- Download and install PHP 7.4 (or later) from the official PHP website for Windows.
- Install PHP Manager for IIS to simplify PHP configuration.
- Configure IIS to use PHP by registering the PHP executable in IIS Manager.
- Download the osTicket installation files from the official website and extract them to the IIS web directory (e.g., C:\inetpub\wwwroot\osTicket).
</p>
<br />
<p>
<img src="https://i.imgur.com/YOUR_SCREENSHOT_3.png" height="80%" width="80%" alt="Setting Up MySQL"/>
</p>
<p>
<b>Step 3: Install and Configure MySQL</b><br />
- Download and install MySQL Server (version 5.7 or higher) on the Windows Server.
- Use MySQL Workbench or the MySQL command line to create a new database for osTicket (e.g., `osticket_db`).
- Create a MySQL user with appropriate permissions for the osTicket database.
- Test the database connection to ensure it’s accessible.
</p>
<br />
<p>
<img src="https://i.imgur.com/YOUR_SCREENSHOT_4.png" height="80%" width="80%" alt="osTicket Installation"/>
</p>
<p>
<b>Step 4: Install and Configure osTicket</b><br />
- Open a web browser and navigate to `http://localhost/osTicket/setup` to start the osTicket installer.
- Follow the on-screen instructions, providing the MySQL database details (hostname, database name, username, and password).
- Complete the installation by setting up the admin user and email configurations.
- Secure the installation by deleting the `/setup` directory and setting appropriate permissions on the configuration file (`ost-config.php`).
</p>
<br />
<h2>Testing and Validation</h2>
<p>
<img src="https://i.imgur.com/YOUR_SCREENSHOT_5.png" height="80%" width="80%" alt="Testing osTicket with Mock Users"/>
</p>
<p>
<b>Step 5: Testing with Mock Users</b><br />
- Created multiple mock user accounts (e.g., End User, Agent, and Admin) to simulate real-world ticketing scenarios.
- Submitted test tickets as an End User to verify ticket creation and notification functionality.
- Logged in as an Agent to respond to tickets, update statuses, and assign priorities.
- Validated Admin functionalities, such as configuring help topics, SLA plans, and user roles.
- Tested email notifications and dashboard reporting to ensure proper operation.
</p>
<br />
<h2>Project Outcome</h2>
This project demonstrates proficiency in setting up a help desk ticketing system using osTicket on a Windows Server environment hosted in Microsoft Azure. Key skills include provisioning cloud infrastructure, configuring web servers (IIS), managing databases (MySQL), and testing ticketing workflows with mock users to ensure functionality.
<h2>Next Steps</h2>
- Explore advanced osTicket configurations, such as integrating with email servers or LDAP for user authentication.
- Automate VM provisioning using Azure CLI or PowerShell scripts.
- Document additional troubleshooting steps for common osTicket issues.

