<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2> Files to Download for Installation</h2>

- ### [Download Now](https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6) 📁

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop (Windows App)
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create a Virtual Machine in Microsoft Azure
- Install osTicket v1.15.8
- Install HeidiSQL
- Install MySQL
- Install PHP
- Install Microsoft Visual C++ Redistributable

<h2>Steps</h2>

![Screen Shot 2024-12-27 at 3 49 03 PM](https://github.com/user-attachments/assets/47a717c8-1561-48e5-9538-1c13940cb73d)
First, start by creating a Windows 10 Virtual Machine (VM) in Azure with at minimum, 2 vcpus and 8 GiB memory. The username and password can be anything you'd like, just make sure to take note of it.
</p>
<br />

![Screen Shot 2024-12-27 at 3 53 29 PM](https://github.com/user-attachments/assets/1ef52ea1-ecb4-45ec-885d-2df8015265b4)
Copy the public IP address of your VM and go to the Windows app. From there, you will add a new PC, paste the IP address, and then you can name it "osTicket". After adding the VM, log into it using the username and password you created.
</p>
<br />

![Screen Shot 2024-12-27 at 4 16 41 PM](https://github.com/user-attachments/assets/d7ab094c-6c3b-4aba-979d-b720acab5e37)
Next, we must install/enable IIS in Windows with CGI. Go to your search bar > Type "Control Panel" > Click "Programs" > "Turn Windows features on or off" > Scroll down to "Internet Information Services" (IIS) and click on it to enable > Expand it by clicking the "+" next to IIS > Expand "World Wide Web Services" > Expand "Application Development Features" > Click the box next to "CGI" and press "ok".
</p>
<br />

![Screen Shot 2024-12-27 at 5 20 42 PM](https://github.com/user-attachments/assets/9257189c-002b-4b8f-b597-99b06552463e)

Now that we have the ISS applied, we will begin installing the PHP manager file. The PHP manager is the programming lanuguage that will allow us to run the osTicket software to run off a web browser. To download, run the PHP program from the files found at the beginning of this demonstration. Agree to all the terms and it will now be in the operating system.
</p>
<br />

![Screen Shot 2024-12-27 at 5 35 00 PM](https://github.com/user-attachments/assets/7fa9d38b-e9b9-438e-9531-570bb0c4c0de)

Next, find the Rewrite Module (rewrite_amd64_en-US.msi), from the "Download Now" link. Agree to all the terms and install.
</p>
<br />

![Screen Shot 2024-12-27 at 5 56 42 PM](https://github.com/user-attachments/assets/ef65f6e9-4868-4033-83c0-a9165c39c7bd)

Now, we'll create the directory C:\PHP. To do this, open File Explorer > type "C:\" in the search bar > Right-click and create a new folder called, "PHP". Download php-7.3.8-nts-Win32-VC15-x86.zip from the "Download Now" link > Extract it by going to where you download the file, Right-click the PHP 7.3.8 file and press "extract all" and browse to the PHP Folder you just created to dump the files in there.
</p>
<br />

![Screen Shot 2024-12-27 at 6 01 02 PM](https://github.com/user-attachments/assets/c95222c9-ef1c-40c9-973c-5bd166dbc135)

We'll now install the VC_resist.x86 file. Agree to all the terms and install until completion.
</p>
<br />

![Screen Shot 2024-12-27 at 6 16 09 PM](https://github.com/user-attachments/assets/722ce84b-af7f-4281-bea5-c84e0eb16d09)

Next, download and install MySQL. Agree to all the terms, click on "Typical" on the following screen and then press install until full completion.
</p>
<br />

![Screen Shot 2024-12-27 at 6 19 13 PM](https://github.com/user-attachments/assets/fa4a7fa0-9b6e-4e89-9124-478f5955bdcb)





![Screen Shot 2024-12-27 at 6 25 17 PM](https://github.com/user-attachments/assets/aa44cb8a-39e0-4dbd-b509-92295c96b932)

Launch the MySQL > Click "standard configuration" and next > create the username and password. Make sure to keep note of them.
</p>
<br />

![Screen Shot 2024-12-27 at 6 36 31 PM](https://github.com/user-attachments/assets/7a1e90d3-0ed3-4b89-881c-c18f0ba8df64)

Go to the search bar > Type "IIS" > Right-click to run as admin. From here we will do the pre-install process for osTicket.
</p>
<br />

![Screen Shot 2024-12-27 at 6 40 20 PM](https://github.com/user-attachments/assets/fe6d7076-e462-4ac9-a66f-2fa16fe8a0de)

Go to PHP Manager > click "Register new PHP version" > browse to the Windows (C:) drive > open the PHP folder > open the "php-cgi" application and press ok.
</p>
<br />

![Screen Shot 2024-12-27 at 6 46 22 PM](https://github.com/user-attachments/assets/9ef48157-8435-422f-acd3-2537a93d6ad6)

Refresh IIS by clicking stop, wait a few seconds, and then click start.
</p>
<br />

![Screen Shot 2024-12-27 at 6 51 07 PM](https://github.com/user-attachments/assets/58e36e57-7e02-48b8-959c-8b3542d63d8f)

Now to start installing osTicket, open a seperate File Exploxer tab > extract the "osTicket-v1.15.8" files > Open Windows (C:) > Click on "inetpub" > Open "wwwroot" > Copy "upload" from the extracted files to "wwwroot" > Within “c:\inetpub\wwwroot”, Rename “upload” to "osTicket". 
</p>
<br />

![Screen Shot 2024-12-27 at 7 02 37 PM](https://github.com/user-attachments/assets/255b8b80-8b24-4395-b78a-1c71fbd70735)

Here, you can see that "osTicket" is now within the "wwwroot" folder.
</p>
<br />

![Screen Shot 2024-12-27 at 7 05 41 PM](https://github.com/user-attachments/assets/ee21f950-dfde-4df4-a610-217797750277)

Go back to the IIS, and stop then start the server to refresh like we did previously.
</p>
<br />

![Screen Shot 2024-12-27 at 7 12 21 PM](https://github.com/user-attachments/assets/b1f3bddb-cf18-4ec0-a5cf-631ece5269fb)

In IIS, go to Sites > Default Web Site > osTicket > In the right corner, click "Browse *.80 (http)". Here it will load the osTicket site.
</p>
<br />

![Screen Shot 2024-12-27 at 7 25 16 PM](https://github.com/user-attachments/assets/b02fb9ba-5fbb-4e2f-a288-0ac9e837c267)

Since some of the extensions necessary to run osTicket correctly are not enabled, go back to IIS > Sites > Default Web Site > osTicket > Double-click on the PHP Manager > Click on "Enable or disable an extension" > Enable the following - "php_imap.dll", "php_intl.dll", "php_opcache.dll" > Refresh the browser on osTicket.

</p>
<br />


![Screen Shot 2024-12-27 at 7 35 38 PM](https://github.com/user-attachments/assets/f9a92220-cf0b-4be0-b95b-73333f02af80)

We'll now rename a file. Go From: "C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php" To: "C:\inetpub\wwwroot\osTicket\include\ost-config.php"
</p>
<br />

![Screen Shot 2024-12-27 at 7 44 43 PM](https://github.com/user-attachments/assets/f1176e97-ae11-4fd8-989a-1e1d5b3c24d9)

Now we must assign permissions to the renamed file. Right-click "ost-config.php" > Properties > Security > Advanced > Disable inheritence > Remove all inherited permissions from this object > Add > Select Principal > Type "everyone" > Press ok > Check "Full Control" and apply the changes.
</p>
<br />

![Screen Shot 2024-12-27 at 7 50 29 PM](https://github.com/user-attachments/assets/da0c118b-f517-4fbb-b043-d6d0a22059fd)

We'll now finish the setup in the browser. Enter a name for the Help Desk and an email.
</p>
<br />

![Screen Shot 2024-12-27 at 7 57 01 PM](https://github.com/user-attachments/assets/9e5eaed9-6399-4cbb-81ea-beb7f9c03afa)

Install HeidiSQL from the downloaded files found in osTicket on the Desktop
</p>
<br />

![Screen Shot 2024-12-27 at 8 01 31 PM](https://github.com/user-attachments/assets/97b670f3-b2a8-457a-a7fa-a648465e921a)

In HeidiSQL, start a new session and have the user and password be "root" for both and then connect to the session.
</p>
<br />

![Screen Shot 2024-12-27 at 8 03 47 PM](https://github.com/user-attachments/assets/670e75af-b04d-4bab-aded-2e550636f279)

Create a new database called "osTicket"
</p>
<br />

![Screen Shot 2024-12-27 at 8 06 32 PM](https://github.com/user-attachments/assets/ac4b06b3-a080-4c61-8a21-a11763333ee8)

Go back to the browser to finish the setup using the credentials below.
</p>
<br />

![Screen Shot 2024-12-27 at 8 08 50 PM](https://github.com/user-attachments/assets/8116dc8c-b3fe-45dd-95b5-e54b3b5ffc3d)

If there were no errors, the setup has been complete. Congratulations!
</p>
<br />

![Screen Shot 2024-12-27 at 8 14 21 PM](https://github.com/user-attachments/assets/c81852d3-7ef6-4163-87ba-7893e8e1277b)

Finally, we'll clean up some of the files. Delete: C:\inetpub\wwwroot\osTicket\setup.
</p>
<br />

![Screen Shot 2024-12-27 at 8 16 45 PM](https://github.com/user-attachments/assets/4042252c-935c-457e-bc0f-b823a861c18c)

Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<br />

![Screen Shot 2024-12-27 at 8 19 11 PM](https://github.com/user-attachments/assets/295042df-08bc-4880-b1c8-77d806794046)

We can now go to the osTicket Admin Panel homepage. Congrats, you have succesfully finished installing osTicket!
</p>
<br />
