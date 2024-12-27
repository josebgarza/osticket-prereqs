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

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
