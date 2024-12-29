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
  <img src="https://i.postimg.cc/nLbwL5tF/os-Ticket-Basic-Install.png"height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">This page is where you will setup where you will name your helpdesk and create the admin user. You do not have to use a real email for either of these but they do need to be different emails. Be sure to take note of your username and password for the admin user login.</h3>
<br />
<p>
  <img src="https://i.postimg.cc/85nZ0Svt/Database-Set-Up.png"height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">Go back to the XAMPP Control Panel and click on the Admin action beside MySQL. This will bring you to the phpmyadmin page shown above. On the left side of the page click new to create a new database. Name it whatever you want to.</h3>
<br/>
<p>
  <img src="https://i.postimg.cc/fW7bhRy3/Database-New-User.png" height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">DOWNLOAD MySQL </h3>
<h3 align="center"> Download and install MySQL, Agree with any terms and agreements up until you get to the password portion. Here you can create a username and password for the database that you'll be using to store the Ticket Information used in osTicket. 
</h3>
<p>
  <img src="https://i.imgur.com/IVpLg40.png"75%" width="100%"/>
<br/>
  <img src="https://i.imgur.com/zdhWXNx.png" height="75%" width="100%" />
</p>
<br/>
<h3 align="center">Install osTicket v1.15.8</h3>
<br />
<p>
  Download osTicket (download from within lab files: link).
</p>
<p>
	Extract and copy the “upload” folder INTO c:\inetpub\wwwroot:
</p>
	<img src="https://i.imgur.com/0MUJLMU.png" height="75%" width="100%" />
	<img src="https://i.imgur.com/1h9goM8.png" height="75%" width="100%" />
<p>
	Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”:
</p>
<p>
	<img src="https://i.imgur.com/pDikkgq.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Reload IIS (Open IIS, Stop and Start the server)</h3>
<br />
<p>
	Go to sites -> Default -> osTicket:
</p>
<p>
	<img src="https://i.imgur.com/QeWNlG3.png" height="75%" width="100%" />
</p>
<p>
	On the right, click “Browse *:80”:
</p>
<p>
	<img src="https://i.imgur.com/3iXhNbi.png" height="75%" width="100%"/>
</p>
<br />
<br />
<h3 align="center">Enable Extensions in IIS: Note that some extensions are not enabled</h3>
<br />
<p>
	Go back to IIS, sites -> Default -> osTicket.
</p>
<p>
	Double-click PHP Manager:
</p>
<p>
	<img src="https://i.imgur.com/LFKo5Hs.png" height="75%" width="100%" />
</p>
<p>
	Click “Enable or disable an extension”.
</p>
<p>
	Enable: php_imap.dll.
</p>
<p>
	Enable: php_intl.dll.
</p>
<p>
	Enable: php_opcache.dll:
</p>
<p>
	<img src="https://imgur.com/a/nrQo0kz" height="75%" width="100%"/>
</p>
<br />
<br />
<h3 align="center">Refresh the osTicket site in your browser, observe the changes</h3>
<br />
<p>
	<img src="https://i.imgur.com/6iSNd4H.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Rename</h3>
<br />
<p>
	From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php.
</p>
<p>
	To: C:\inetpub\wwwroot\osTicket\include\ost-config.php:
</p>
<p>
	<img src="https://i.imgur.com/TEw71SD.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Assign Permissions: ost-config.php</h3>
<br />
<p>
	Disable inheritance -> Remove All:
</p>
<p>
	<img src="https://i.imgur.com/1QtRWEF.png" height="75%" width="100%" />
</p>
<p>
	New Permissions -> Everyone -> All:
</p>
<p>
	<img src="https://i.imgur.com/YzsMXNX.png" height="75%" width="100%" />
</p>
<p>
	<img src="https://i.imgur.com/k7x9yGR.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Continue Setting up osTicket in the browser (click Continue)</h3>
<br />
<p>
	Name Helpdesk.
</p>
<p>
	Default email (receives email from customers):
</p>
<p>
	<img src="https://i.imgur.com/rvMvlNC.png" height="75%" width="100%" />
	<img src="https://i.imgur.com/YszhIpl.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Download and Install HeidiSQL</h3>
<br />
<p>
	<img src="https://i.imgur.com/AEg0b2P.png" height="75%" width="100%" />
</p>
<p>
	Create a new session, root/Password1.
</p>
<p>
	Connect to the session:
</p>
<p>
	<img src="https://i.imgur.com/9t51ApR.png" height="75%" width="100%" "/>
</p>
<p>
	Create a database called “osTicket”:
</p>
<p>
	<img src="https://i.imgur.com/vXzmQqg.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Continue Setting up osTicket in the browser</h3>
<br />
<p>MySQL Database: osTicket</p>
<p>
	MySQL Username: root
</p>
<p>
	MySQL Password: Password1:
</p>
<p>
	<img src="https://i.imgur.com/akDyber.png" height="75%" width="100%" />
</p>
<p>Click “Install Now!”</p>
<p>Congratulations, hopefully it is installed with no errors!</hp>
<p>
	<img src="https://i.imgur.com/J5omRoE.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Clean up</h3>
<br />
<p>
	Delete: C:\inetpub\wwwroot\osTicket\setup:
</p>
<p>
	<img src="https://i.imgur.com/eg0ZPG3.png" height="75%" width="100%" />
</p>
<p>
	Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php:
</p>
<p>
	<img src="https://i.imgur.com/n6k46XL.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)</h3>
<br />
<p>
	<img src="https://i.imgur.com/8wvWH0H.jpg" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center"> Congrats, You've Finished Installing osTicket.</h3>
