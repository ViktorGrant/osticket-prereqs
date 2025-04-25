<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### coming soon

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Start 20 step process</h2>

- Step 1: Download the  osTicket-Installation-Files.zip and unzip/extract

- Step 2: Install / Enable IIS in Windows WITH CGI
  
  &emsp;- Control panel -> Programs -> Uninstall Programs -> Turn Windows features onoff
  
  &emsp;- Check Internet Information Services
  
  &emsp;- www  services -> App Dev Features -> CGI

- Step 3: Inside osTicket folder Install

  &emsp;- PHP (PHPManagerForIIS_V1.5.0.msi)

  &emsp; - Rewrite module (rewrite_amd64_en-US.msi)



- Step 4: Create a folder on C drive called “PHP”

  
- Step 5: in osTicket folder extract all from -> (php-7.3.8-nts-Win32-VC15-x86.zip) into PHP folder

- Step 6: install VC_redist.x86

- Step 7: install mysql-5.5.62-win32
  
  &emsp;- Launch standard configuration
  
  &emsp;- Username: root
  
  &emsp;- Password: root




<h2>osTicket Installation Files</h2>

<p>
<img width="1280" alt="image 1 os Ticket Install" src="https://github.com/user-attachments/assets/013f44f1-f185-4422-867b-34d51bbc7566" />
</p>
<p>
This is kinda what your screen should look like. You got the “osTicket” file opened on the left and the normal folder opened in the middle. The two folders on the left are the osTicket folders, one is the unzipped/extracted version of the other.
</p>
<br />

- Step8: open IIS as admin -> start -> search “iis” -> run as adim

- Step9: Register PHP from within IIS -> php manager -> register new php version -> browse to php folder inside get “php-cgi”

- Step 10: refresh IIS -> top left of IIS under “connections” right click “practice-osTicket” -> click stop -> wait -> click start

<p>
<img width="1280" alt="image 2 start and stop ISS" src="https://github.com/user-attachments/assets/adb338f1-5c63-4ba7-a6af-249f873eea76" />
</p>
<p>
This is the ISS and how to (Start | Stop) it

- Step 11: Install “osTicket-v1.15.8.zip” -> extract -> it will open folder w “scripts | upload”
  
  &emsp;- Put the “upload” folder into “c:\inetpub\wwwroot” and rename “upload” to “osTicket”

- Step 12: reload ISS (stop | start)

- Step 13: Load os ticket site
  
   &emsp;- ISS -> sites -> default -> osTicket
  
   &emsp;- On the right click “Browse*.80(http)” (this should pull up the osTicket site)

<p>
<img width="1280" alt="image 3 osTiket page" src="https://github.com/user-attachments/assets/3a135bd2-c1f1-4d1a-9012-fd90583cbe5b" />
</p>
<p>
This is how osTicket should look when it pulls up in the web browser.
</p>
<br />

- Step 14: Notice some extensions are not enabled

  &emsp;- ISS -> Sites -> Default sites -> osTicket

  &emsp;- ISS -> Sites -> Default sites -> osTicket

  &emsp;- ISS -> Sites -> Default sites -> osTicket

  &emsp;&emsp;- Enable: php_imap.dll

  &emsp;&emsp;- Enable: php_intl.dll

  &emsp;&emsp;- Enable: php_opcache.dll

  &emsp;- Refresh osTicket browser and see they are enabled

- Step 15: rename ost-config.php

  &emsp; - From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
  
  &emsp; - From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php

- Step16: Assign permissions - ost-config.php

  &emsp; - Right click-> properties -> security -> advancted -> Disable inheritance -> remove all

  &emsp; - Click add -> principal -> Everyone -> ok -> check “full control” -> ok ok ok (now osTicket has control to the configuration file)

<p>
<img width="497" alt="image 4 like this " src="https://github.com/user-attachments/assets/7c89bbe1-bd7c-48da-b65f-07e7e85a38a7" />
</p>
<p>
The access should look something like this
</p>
<br />

- Step 17: Set up rest of osTicket

  &emsp; - username : testtoad

  &emsp;- Password: Password1

- Step 18: from “osTicket installation files” install “HeidiSQL_12.3.0.6589_Setup”

  &emsp;- Double click -> check accept box -> ok ok ok

  &emsp;- Create new session -> click new root/root

  &emsp;- Create data base called “osTicket” -> rightclick dolphin -> create new -> database

- Step19: continue setting up osTicket from browser

  &emsp;- MySQL Database: osTicket

  &emsp;- MySQL Username: root

  &emsp;- MySQL Password: root

  &emsp;- Install now

- Step 20: Congratulations osTicket is installed!

  &emsp;- login page: http://localhost/osTicket/scp/login.php

  &emsp;&emsp;- Username: testtoad

  &emsp;&emsp;- Password: Password1

  &emsp;- Enter Tickets: http://localhost/osTicket/







  
