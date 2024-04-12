<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Active Directory Deployed in Oracle VirtualBox</h1>
This tutorial outlines the implementation of Active Directory within VirtualBox.<br />

<h2>Environments and Technologies Used</h2>

- Oracle VM VirtualBox
- Active Directory Domain Services


<h2>Programing Language</h2>

- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

Step 1: Creating Vitual Boxes
- Download VM Virtaul Box from Oracle website.
- Download Windows 10 iso and Windows Server 2022 iso files from Windows website.
- Open Virtual Box and select "New".
- Name the VM and select Windows Server 20222 iso with at least 8GB of RAM, 1 core processor, and 250GB of storage memeory.
<p>  
<img src="https://github.com/AllanMontalvo/Virtualbox-Active-Directory/assets/135927674/2c6c5e6a-63a4-47e7-91db-cfbf53b65f34" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
- Repeat the same process for creating a Windows 10 VM.
<p>
<img src="https://i.imgur.com/oyvca2r.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


Step 2: Setup DC-1
- Start up DC-1 VM
- Open System Properties and under "Computer Name" tab, select "Change" to rename computer.
- Type "DC-1" in computer name and select "Ok"
- Restart the computer and open "About this PC" to see the change of computer name.
<p>
  <img src="https://github.com/AllanMontalvo/Virtualbox-Active-Directory/assets/135927674/ff355598-8912-4d6c-ac97-fd03c46cfc2d" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

Step 3: Download Active Directory
- Open Server Manager
- Under "Manage", select "Add Roles and Features"
- Follow the steps and add "Active Diretory Domain Services" role.
- Prompted for deployment configuration, select "Add a new forest" and create a domain name (e.g. mynetwork.net)
- Continue with the configuration and restart DC-1
- Log back in as mynetwork\labuser
- Step 4

<h2>Deployment and Configuration Steps</h2>


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

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
