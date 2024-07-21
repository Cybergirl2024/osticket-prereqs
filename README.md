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


<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/ZrvDvfN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I created an Azure resource group called labcc1133 and a virtual machine to download the os-ticket on.
</p>
<br />

<p>
<img src="https://i.imgur.com/H9JRRdP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next I logged into my Windows virtual machine by using remote desktop connection and using the public IP address for this virtual machine. I also used the username and password I created to log in to the virtual machine.
</p>
<br />

<p>
<img src="https://i.imgur.com/B7QU0jz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I configured Windows features by going to the control panel > programs > Turn Windows Features On and Off and configure the features. By doing this I am allowing this virtual machine to access IIS. So when I type 127.0.0.1 into the web browser of Microsoft Edge I should be able to access the IIS.
</p>
<br />

<p>
<img src="https://i.imgur.com/GxeF74k.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I am now able to get into Internet Information Services on the Microsoft Edge web browser. With IIS enabled os-Ticket can now run. Next we will begin the process of downloading Os-Ticket.
</p>
<br />

<p>
<img src="https://i.imgur.com/o5l7ITV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The first file you need to download is PHP manager for IIS. 
</p>
<br />

<p>
<img src="https://i.imgur.com/U5PugeD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The next file you need to download is rewrite_amd_64 and for the next few steps we are going to be downloading the files os-Ticket needs to run on.
</p>
<br />

<p>
<img src="https://i.imgur.com/Gi8w6Pe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I created a C:\PHP folder to extract the next file we download into this folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/JUwn8E0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The next file I downloaded was php 7.3.8 file. This is the file I am going to extract all the content in this file and put it into the PHP file I created in the last step.
</p>
<br />

<p>
<img src="https://i.imgur.com/dtTAJ6s.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I extracted all the content in the php 7.3.8 zip files and put it into the PHP folder I created.
</p>
<br />

<p>
<img src="https://i.imgur.com/ZhsLSnJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The final file I downloaded was mysql. These are the options I picked to set up mysql:
Typical Setup >
Launch Configuration Wizard (after install) >
Standard Configuration >
password1
</p>
<br />

<p>
<img src="https://i.imgur.com/CfOXJtw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I typed IIS in the windows search bar and ran it as an admin. 
</p>
<br />

<p>
<img src="https://i.imgur.com/WSnX1So.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I am now in IIS and the first thing I did was restart the application.
</p>
<br />

<p>
<img src="https://i.imgur.com/wKV9vsd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next I went to PHP manager and registered in a new version of the manager.
</p>
<br />

<p>
<img src="https://i.imgur.com/wKV9vsd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next I went to PHP manager and registered in a new version of the manager. After I finished doing that I restarted IIS again so it can register the new version of the PHP manager.
</p>
<br />

<p>
<img src="https://i.imgur.com/d82Xbiv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I downloaded os-Ticket. These are all the files you should have downloaded in order to make sure os-Ticket runs properly.
</p>
<br />

<p>
<img src="https://i.imgur.com/Q8zmoFO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I extracted the upload folder from the os-Ticket zip file and place it into the wwwroot folder. I also renamed the folder os-Ticket so I won't get confused on what folder I am using.
</p>
<br />

<p>
<img src="https://i.imgur.com/lqz9LNI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The next thing I did was restart IIS again, then I navigated to os-Ticket > Sites > Default Web Sites >  osTicket and I clicked on Browse 80 to the right of the screen. This should give me access to the os-Ticket browser.
</p>
<br />

<p>
<img src="https://i.imgur.com/25RuBDD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now I have access to the os-Ticket browser.
</p>
<br />

<p>
<img src="https://i.imgur.com/DBWSZEW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I went back to IIS, sites > default > osTicket, I clicked on PHP Manager, next I went to enable or disable an extension. Then I enabled php_imap.dll, php_intl.dll, php_opcache.dll. Then I refreshed the osTicket site and these extensions should be checked off.
</p>
<br />

<p>
<img src="https://i.imgur.com/0oDhZq2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now those extensions that I enabled are checked on the os-Ticket site.
</p>
<br />

<p>
<img src="https://i.imgur.com/jeI1EUQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The next step I took was to rename os-sampleconfig to os-config in the following file path in the image.
</p>
<br />

<p>
<img src="https://i.imgur.com/SJj0SP6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I modified the permissions for the os-config file to everyone and gave them full control.
</p>
<br />

<p>
<img src="https://i.imgur.com/wIP4yoz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I clicked on continue for the os-Ticket to fill out the information on this page.
</p>
<br />

<p>
<img src="https://i.imgur.com/JcsR3Hm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I downloaded Heidi Sql and created a new session.
</p>
<br />

<p>
<img src="https://i.imgur.com/GxW1XyT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I filled in the last of the information for the os-Ticket and Installed the it.
</p>
<br />

<p>
<img src="https://i.imgur.com/eSrtQ1T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I logged into the osTicket with the username and password I created and this is the end of the installation process.
</p>
<br />

<p>
<img src="https://i.imgur.com/pLwaOyp.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
These are all the files you need to have in order to install and run os-Ticket properly.
</p>
<br />









