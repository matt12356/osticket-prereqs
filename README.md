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

- Azure with subscription to set up Virtual Machine
- Remote desktop connection
- Enable IIS
- Install php manger for IIS
- Install rewrite module
- Install PHP 7.3.8
- Install VC redist.x.86.exe
- INSTALL MYSQL 5.5.62 set up username and password


<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/MeQ4hJR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Create a Resource group in Azure then create a virtual machine and place the virtual machine inside the resource group. Once completed, copy the public IP address of the virtual machine and paste the address into remote desktop connection and connect. Once connected we will begin to download the pre reqs for Osticket. 
</p>
<br />

<p>
<img src="https://i.imgur.com/apMo55g.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
First go to world wide web services applications devlopment and enable CGI. Then install all the pre reqs for osticket which include PHP manger for IIS, Rewrite module,
  PHP 7.3.8, VC redistx86.exe, and My sql. Make sure when you donwload PHP manger for IIS you create a  PHP folder to unzip its contents. When MY SQL is done being installed make sure you click typical set up, launch configuration wizard after install, click standard configurtion and set the password to something you will remember.
</p>
<br />

<p>
<img src="https://i.imgur.com/crlkuT8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now install osticket v1.15.8, once installed extract and copy "upload" folder to c:\inetpub\wwwroot and within the folder switch folder name from "upload" to "osticket". Restart IIS and once loaded back up go to sites then default then osticket and on the right click browse ".80". This will bring you to osticket installler at this point go back into IIS then click php manager to enable a few extensions. Extensions to enable are php_impa.dll, php_intl.dll, and php_opcache.dll then refresh osticket installer site. Now go into C drive then wwwroots\osticket\include and change "ostsampleconfig.php" to "ost-config.php" assign permissions disable inhertiance click remove all and then for new permissions set everyone and click all. Now go back to osticket browser and set up information for helpdesk, after that install HeidiSQL and open it up. Create a new session using MYSQL username and password you created and call it osticket. Go back to osticket installer browser where it ask for database username\pasword use MYSQL information and install.
</p>
<br />
