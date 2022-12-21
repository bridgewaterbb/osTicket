<p align="center">
<img src="https://i.imgur.com/IWhAdIY.png" alt="osTicket"/>
</p>

<h1>Installation and configuration of osTicket (Help Desk Ticketing System)</h1>
In this lab I installed Microsoft IIS (Internet Information Services), osTicket, and osTicket's dependencies. I then configured osTicket and explored its utility.<br />


<h2>Technology Utilized</h2>

- Microsoft Azure (Virtual Machine/Cloud)
- Remote Desktop
- osTicket
- Microsoft IIS (Internet Information Services)
- HeidiSQL
- Web Platform Installer

<h2>Operating Systems</h2>

- Windows 10 (21H2)

<h2>Overview of Tasks</h2>

- Enable IIS in Windows 10
- Install Web Platform Installer
- Install osTicket Dependencies
- Install osTicket Core v1.16.5
- Configure osTicket
- Install HeidiSQL and create database
- Configure osTicket in browser

<h2>Deployment and Configuration</h2>

<p>
<img src="https://i.imgur.com/NG2oAXN.png" height="80%" width="80%" alt="Enabling IIS"/>
</p>
<p>
I provisioned a Windows 10 Pro machine through Microsoft Azure. I then connected to this machine through RDP (Remote Desktop Protocol). I enabled IIS (Internet Information Services) on this machine and installed Web Platform Installer. I then installed the dependencies for osTicket through the Web Platform Installer: PHP(x86) up to 8.0, MySQL 5.5, and PHP Manager for IIS 1.5.0. There were failures during this process. I found the dependencies still needed in a web browser and installed them seperately. I then installed osTicket, v1.16.5. The osTicket file was unzipped and the "upload" file was moved to C:\inetpub\wwwroot and renamed osTicket. 
</p>
<br />

<p>
<img src="https://i.imgur.com/jxTTNRq.png" height="80%" width="80%" alt="Heidi SQL"/>
</p>
<p>
In the osTicket folder in IIS, I entered the PHP Manager. I then enabled php_imap.dll, php_intl.dll, and php_opcache.dll. I then browsed to where the machine was hosting the osTicket web app to verify it was able to be hosted. I then renamed the configuration file and gave everyone all permissions (After install these permissions were changed to read only). I then installed HeidiSQL and connected to a session with the credentials I established when installing MySQL. In HeidiSQL I created a new database for osTicket. I then returned to osTicket in the browser and finished the intial setup. 
</p>
<br />

<p>
<img src="https://i.imgur.com/BNOaV9Q.png" height="80%" width="80%" alt="osTicket"/>
</p>
<p>
Once in the dashboard of osTicket with our installation admin account I was able to further configure osTicket. From the admin panel I created agents, departments, teams, users, and SLAs (Service Level Agreements). As an added user I submitted tickets from the osTicket submission page. From the agent panel I was able to view submitted tickets and assign them to agents. As an admin I experimented with changing priority levels of tickets and assigning tickets to agents. 
</p>
<br />
