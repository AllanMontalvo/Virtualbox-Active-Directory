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

**Step 1: Creating Vitual Boxes**
- Download VM Virtaul Box from Oracle website.
- Download Windows 10 iso and Windows Server 2022 iso files from Windows website.
- Open Virtual Box and select "New".
- Name the VM and select Windows Server 20222 iso with at least 8GB of RAM, 1 core processor, and 250GB of storage memeory.
<p>  
<img src="https://github.com/AllanMontalvo/Virtualbox-Active-Directory/assets/135927674/2c6c5e6a-63a4-47e7-91db-cfbf53b65f34" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>

- Repeat the same process for creating a Windows 10 VM.
<p>
<img src="https://i.imgur.com/oyvca2r.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>

**Step 2: Setup DC-1**
- Start up DC-1 VM.
- Open "About this PC" and select "Advance system settings".
- Under "Computer Name" tab, select "Change" to rename computer.
- Type "DC-1" in computer name and select "Ok".
- Restart the computer and open "About this PC" to see the change of computer name.
<p>
  <img src="https://github.com/AllanMontalvo/Virtualbox-Active-Directory/assets/135927674/ff355598-8912-4d6c-ac97-fd03c46cfc2d" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

**Step 3: Download Active Directory**
- Open Server Manager.
- Under "Manage", select "Add Roles and Features".
- Follow the steps and add "Active Diretory Domain Services" role.
<p>
  <img src="https://github.com/AllanMontalvo/Virtualbox-Active-Directory/assets/135927674/6815d963-caaa-4b73-b453-6ff1bdf8234f" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Prompted for deployment configuration, select "Add a new forest" and create a domain name (e.g. mynetwork.net).
<p>
  <img src="https://github.com/AllanMontalvo/Virtualbox-Active-Directory/assets/135927674/789c9da8-24e9-44e7-b42a-f574d8bc02e6" height="80% width="80%" alt="Disk Sanitization Steps"/>
</p>

- Continue with the configuration and restart DC-1.
- Log back in as mynetwork\Administrator.

**Step 4: DC-1 IP Configuration**
- Open control panel and select "Network and Sharing Center".
- Select "Change adapter settings" and double-click "Ethernet".
- Look for "Internet Protocol Version 4 (TCP/IPv4) and double-it.
- Manually setup IP addresses (e.g. IP address:10.1.10.2, Subnet:255.0.0.0, Default gateway:10.1.10.1).
- Manually set DNS server address (e.g. Preferred DNS server:10.1.10.2, Alternate DNS server:10.1.10.1).
<p>
<img src="https://github.com/AllanMontalvo/Virtualbox-Active-Directory/assets/135927674/bf418515-d03b-4bd0-950b-628fa0cdb47d" height="40% width="40% alt="Disk Sanitization Steps"/>
</p>

**Steps 5: Setup Client-1**
- Start up Client-1 VM.
- Open "About this PC" and select "Advance system settings.
- Under "Computer Name" tab, select "Change" to rename computer.
- Type "Client-1" in computer name and select "Ok".
- Restart the computer and open "About this PC" to see the change of computer name.
<p>
  <img src="https://github.com/AllanMontalvo/Virtualbox-Active-Directory/assets/135927674/36ed42bf-a885-4cd3-8102-651a8ebf6c83" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>


**Step 6: Client-1 IP Configuration**
- Open control panel and select "Network and Sharing Center"
- Select "Change adapter settings" and double-click "Ethernet"
- Look for "Internet Protocol Version 4 (TCP/IPv4) and double-it.
- Manually setup IP addresses (e.g. IP address:10.1.10.3, Subnet:255.0.0.0, Default gateway:10.1.10.1).
- Manually set DNS server address (e.g. Preferred DNS server:10.1.10.2, Alternate DNS server:10.1.10.1).

<p>
  <img src="https://github.com/AllanMontalvo/Virtualbox-Active-Directory/assets/135927674/9654f0ad-95b7-4338-a7f6-cf99e7921b9a" height=80% width="80%" alt="Disk Sanitization Steps">
</p>

**Step 7: Connectivity**
- On VirtualBox Manager, select "DC-1" and go to "Settings".
- Under "Network", change "NAT" to "Host-only Adapter".
- Checked "Cable Connected" under "Advance" and select "Ok".
- Repeat the same step for "Client-1".
<p>
  <img src="https://github.com/AllanMontalvo/Virtualbox-Active-Directory/assets/135927674/8d0f4792-c23a-45ad-848d-5d516386662c" height="80% width="80%" alt="Disk Sanitization Steps">
</p>

**Step 8: Verify Connectivity**
- Open command prompt on "Client-1".
- ping DC-1 with command: ping <DC-1's IP address>
<p>
<img src="https://github.com/AllanMontalvo/Virtualbox-Active-Directory/assets/135927674/6c70a7c9-13e2-4864-8b2a-8c750e9ce720" height=80%" width="80%" alt="Disk Sanitization Steps">
</p>



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
