# osTicket-Installation
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites *Coming Soon*]()

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- osTicket Installation files
- Heidi SQL

<h2>Installation Steps</h2>

<p>
Lets get started , create a virtual machine in microsoft azure and run the operation system windows 10 with 2 - 4 CPU and atleast 8GB of ram. See network security groups if you want to learn how because its very important you understand the basics of creating vm and why!
</p>
<p>
To enable IIS on your Windows virtual machine, open the Control Panel, click on "Uninstall a Program," and then select "Turn Windows features on or off" from the left-hand menu. In the list of features that appears, locate and enable "Internet Information Services (IIS)" by checking the box next to it, and then click "OK" to apply the changes.
<p>
<img src="https://imgur.com/g7POZJF.png" height="80%" width="80%" alt="Steps 1"/>
</p>
<p>
Google the osticket folder and then install the items highlighted first.
<img src="https://imgur.com/69QnSI3.png" height="80%" width="80%" alt="Steps 2"/>
</p>
<br />

<p>
Next download osTicket. Then extract and copy the "upload" folder into c:\inetpub\wwwroot. Afterwards rename the folder to osTicket
<img src="https://imgur.com/SrntV7M.png" height="80%" width="80%" alt="Steps 3"/>
<img src="https://imgur.com/2SpCnKU.png" height="80%" width="80%" alt="Steps 4"/>
</p>
<p>
Alright almost done !, Open IIS Manager and restart the server this will be located on right where you see manage websites. Once inside IIS manager go to Sites->Default->osTicket on the right, click "Browse*.80" from there your default browser should open osTicket webserver.
</p>
<br />
<p>
<img src="https://imgur.com/AvBJHQe.png" height="80%" width="80%" alt="Steps 5"/>
</p>
<p>
Open IIS Manager and enable the necessary PHP extensions. Navigate to Sites → Default → osTicket, then double-click on PHP Manager. Select "Disable or enable an extension", and enable both "php_intl.dll" and "php_opcache.dll". Once done, refresh the osTicket webserver, and you should see that the "Intl Extension" is now enabled.
<img src="https://imgur.com/F7fcDSY.png" height="80%" width="80%" alt="Steps 6"/>
</p>
<br />

<p>
Navigate to C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php and rename the file to C:\inetpub\wwwroot\osTicket\include\ost-config.php. Next, assign the appropriate permissions to the ost-config.php file. Disable inheritance, remove all existing permissions, and then assign new permissions by granting Everyone full access.
<img src="https://imgur.com/I0IzDY4.png" height="80%" width="80%" alt="Steps 7"/>
<img src="https://imgur.com/0AICQ8m.png" height="80%" width="80%" alt="Steps 7.5"/>
</p> 
<p>
<p>
Congrats you're done, just finish signing up and you're good to go!
<img src="https://imgur.com/w6YKZbD.png" height="80%" width="80%" alt="Steps 8"/>
</p>
