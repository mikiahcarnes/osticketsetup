<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png"/>
</p>

<h1> How to Install osTicket </h1>
This is an easy guide to installing a help desk ticketing system called osTicket.<br/>


<h2> Software & Technologies  Used</h2>

- Windows 10<br/>
- VMware Workstation Pro</br>
- XAMPP v8.2.12</br>
- osTicket v1.18.1

  <h2> Objectives </h2>

- Create Windows 10 virtual machine
- Install XAAMP (latest version)
- Install osTicket (latest version)

  <h2>Steps</h2>
<h3 align="center">Create Windows 10 Virtual Machine</h3>
<br />
<p>
<h3 align="center">Note: Before you continue, you will want to download the <a href="https://www.microsoft.com/en-us/software-download/windows10" target="_blank">Windows 10</a> iso file to your system.</h3>
<br />
</p>
<p>
	
<div align="center">
  <a href="https://youtu.be/CMGa6DsGIpc">
    <img src="https://img.youtube.com/vi/CMGa6DsGIpc/0.jpg" alt="Watch the video" height="75%" width="50%">
  </a>
</div>

</p>
<p>
<h3 align="center">I recommend using Oracle VirtualBox to host your virtual machine. Use the video above for a simple walkthrough. You don't need more than 4gb(4096mb) memory, 2 cpu (1 if you have limited resources), and 50-60gb storage. </h3>
<br />
</p>
<p>
	<img src="https://i.postimg.cc/CLzj7VN8/XAMPPControl-Panel.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">After you set up the Windows 10 virtual machine, you will want to open the browser in your machine, the default will be Edge, and download the latest version of <a href="https://www.apachefriends.org/download.html" target="_blank">XAMPP</a>. During installation, leave everything default. After you have XAMPP installed, go ahead and start Apache and MySQL. </h3>
<br />
<p>
	<div align="center">
  <img src="https://i.postimg.cc/1tztSwJj/os-Ticket-Install-Page.png" alt="Image 1" height="75%" width="45%">
  <img src="https://i.postimg.cc/VsXCRQdG/os-Ticket-Git-Hub.png" alt="Image 2" height="75%" width="45%">
</div>
	
</p>
<br />
<h3 align="center">Now that XAMPP is up and running, it's time to download the osTicket .zip folder. You can find the latest version of osTicket <a href="https://osticket.com/download/" target="_blank">here</a>. I circled what you need to click on each page to download the osTicket .zip folder only. After downloading the osTicket .zip folder, right-click it and extract all. After you extract the osTicket folder, I suggest renaming it to "osTicket." </h3>
<br />
<p>
	<img src="https://i.postimg.cc/zfN9gyXj/Path-Foros-Ticket-In-XAMPP.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Now, we want to move the unzipped osTicket folder into your XAMPP server. You can do this by either right-clicking and copying the folder, then pasting it in the htdocs folder, or clicking ctrl + x and then pasting it to the htdocs folder. The path for this is "C:\xampp\htdocs." After you paste the file, it should look like the image above. </h3>
<br />
<p>
  <img src="https://i.postimg.cc/J4tx0MFw/localhostpath.png" height="75%" width="100%"/>
</p>
<br />
<h3 align="center">Go back to the XAMPP control panel, make sure Apache and MySQL are started, and click on the Admin action beside Apache. It will likely open into the "localhost/dashboard/" link. Change dashboard to osTicket or whatever you changed the name of your osTicket folder to. It should look like the picture above. Click on the upload folder and click continue on the setup page for a default setup. You can always enable the other features later if you need them.</h3>
<br />
<p>
  <img src="https://i.postimg.cc/xTRXwz5n/pathforos-confignamechange.png"height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">The next page will tell you that you are missing the configuration file. The above picture is the path to the ost-sampleconfig.php file which you need to rename to ost-config.php.</h3>
<br />
<p>
  <img src="https://i.postimg.cc/nLbwL5tF/os-Ticket-Basic-Install.png" height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">This page is where you will setup where you will name your helpdesk and create the admin user. You do not have to use a real email for either of these but they do need to be different emails. Be sure to take note of your username and password for the admin user login.</h3>
<br />
<p>
  <img src="https://i.postimg.cc/85nZ0Svt/Database-Set-Up.png" height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">Go back to the XAMPP Control Panel and click on the Admin action beside MySQL. This will bring you to the phpmyadmin page shown above. On the left side of the page click new to create a new database. Name it whatever you want to.</h3>
<br/>
<p>
  <img src="https://i.postimg.cc/4xzrYK8L/Login-Info-Database.png" height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">Now we need to make a new user for the database. After the database is created you will see it to the left of the page at the bottom. Click on it and click on the privileges tab and click on add user account. You can name it whatever you what, but make sure the Host name is set to Local and localhost. Again, remember to take note of your username and password. Then, scroll down a bit and you will see the Global privileges section, go ahead and check all. Then scroll all the way down and click Go. After the database has been made go back to the osTicket setup page and type in the into. MySQL Hostname, MySQL Database, MySQL Usename, and MySQL Password.</h3>
<p>
  <img src="https://i.postimg.cc/T1hdkQ9S/After-Install.png" height="75%" width="100%" />
</p>
<br/>
<h3 align="center">Your install page will look different from the one above, but nonetheless. You have now installed osTicket! You can now follow the instructions for Config file permissions. After that head over to the Admin Panel, which you will see a link to on the right of the page, and continue with configuring osTicket.</h3>
