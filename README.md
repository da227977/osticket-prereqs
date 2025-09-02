<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating System Used </h2>

- Windows 11</b> (24H2)

<h2>List of Prerequisites</h2>

-  Extract files for osTicket installation
-  Install and enable Internet Information Services (IIS)
-  Install PHP Manager for IIS and Rewrite Module
-  Create the directory C:\PHP; install VC redist.x86.exe. and MySQL 5.5.62
-  Open IIS as an Admin, register PHP from within IIS and reload IIS
-  Ready to install osTicket v1.15.8


<h2>Installation Steps</h2>

<p>
<img width="1620" height="788" alt="image" src="https://github.com/user-attachments/assets/b039d7e8-96ca-412a-937e-dde039d714c5" />
</p>
<p>
Go to the "osTicket-Installation-Files" folder, unzip/extract all "osTicket-v1.15.8". Copy the "upload" folder into "C:\inetpub\wwwroot". Within "C:\inetpub\wwwroot", rename "upload" to "osTicket".
</p>
<br />

<p>
<img width="1620" height="978" alt="image" src="https://github.com/user-attachments/assets/50395cd0-7a51-46ad-96f9-669be1765ea8" />
</p>
<p>
A new folder will be created, "osTicket-v1.15.8". Open the folder and you will see two other folders, "scripts" and "upload". Copy the "upload" folder into "C:\inetpub\wwwroot". 
</p>
<br />

<p>
<img width="1620" height="978" alt="image" src="https://github.com/user-attachments/assets/1abe56e8-ccb7-4fb7-b016-3c053cd2bedb" />
</p>
<p>
Within "C:\inetpub\wwwroot", rename "upload" to "os Ticket". 
</p>
<br /> 

<p>
<img width="1952" height="978" alt="image" src="https://github.com/user-attachments/assets/068a97d4-3680-4902-b8b2-6fb5ea7cb62a" />
</p>
<p>
Reload IIS (Open IIS, Stop and Start the server). Now you can attempt to load the osTicket site. Go to "sites", "Default Web Site", "osTicket" and then on the right click "Browse *.80 (http)".   
</p>
<br />

<p>
<img width="1204" height="1340" alt="image" src="https://github.com/user-attachments/assets/316e367d-df98-48c5-a80d-26be2cb6e86e" />
</p>
<p>
If successful you will be taken to the "osTicket Installer" site. You will notice that some extensions are not enabled.
</p>
<br />

<p>
<img width="1204" height="1340" alt="image" src="https://github.com/user-attachments/assets/fb4cfcd9-7680-4eac-b167-360d1f6dd4aa" />
</p>
<p>
In order to enable required extensions go back to "IIS", "Sites", "Default Web Site", and "osTicket". Click on "PHP Manager" and then on "Enable or disable an extension". Find and enable the following: "php_imap.dll", "php_intl.dll", and "php_opcache.dll". Refresh the "osTicket" site in your browser and observe the changes.
</p>
<br />

<p>
<img width="1780" height="1108" alt="image" src="https://github.com/user-attachments/assets/89e51b01-cf2a-4794-ba07-a320063fc550" />
</p>
<p>
Rename "ost-sampleconfig.php" to "ost-config.php". Browse to the following path; "C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php". It is very important that you do not make any typos when renaming. It must read "ost-config.php". 
</p>
<br />

<p>
<img width="714" height="489" alt="image" src="https://github.com/user-attachments/assets/3e139e51-ed43-424b-9dcb-c51ea7aaba93" />
</p>
<p>
Permissions need to be assigned to "ost-config.php". Right click on file and go to "Properties", "Security", "Advanced" and then click on "Disable inheritance". Select and click on "Remove all inherited permissions from this object.", there are now no permissions. Click on "Add" then "Select a principal" and type in "everyone" (this is only for use in the lab as you would not add "everyone" in real life for security reasons). Click "Ok" then check "Full control" and click "Apply" then "Ok". Everyone should now have full control in "ost-config.php".
</p>
<br />

<p>
<img width="1774" height="1582" alt="image" src="https://github.com/user-attachments/assets/0fbab69c-5877-4bb0-bf00-1e01c8456f92" />
</p>
<p>
Go back to osTicket Installer website and click on "Continue" and fill in required fields. 
</p>
<br />

<p>
<img width="1384" height="1154" alt="image" src="https://github.com/user-attachments/assets/d089b15e-cd70-481c-9e9a-93038302488e" />
</p>
<p>
Create a database specific to osTicket and provide credentials. Go to "osTicket-Installation-Files" folder, find and install "HeidiSQL". Once installed click on "New" and then fill in the "User" (root) and "Password" (root), then click "Open". A connenction will then be opened to our database. In the upper left click on the dolphin symbol "Unnamed", then "Create new" and "Database". For database name type "osTicket" and click "Ok". Database has now been created.  
</p>
<br />

<p>
<img width="1372" height="1532" alt="image" src="https://github.com/user-attachments/assets/04a20ac4-0ae5-4055-836b-63a617a7b011" />
</p>
<p>
To continue setup go back to "osTicket Installer" in the browser. Fill out Database Settings. 
MySQL Database: "osTicket", MySQL Username: "root", and My SQL Password: "root". Click "Install Now".
</p>
<br />

<p>
<img width="755" height="591" alt="image" src="https://github.com/user-attachments/assets/b24d8230-906c-45f5-89ab-34d2540c3155" />
</p>
<p>
Upon completion you should see a window on the site congratulating you on successfully installing osTicket.
</p>
<br />
