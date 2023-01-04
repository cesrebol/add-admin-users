<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Create an Admin and Normal User Account in AD (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory and creating an admin and users.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- In Active Directory Users and Computers, create an Organizatinal Unit(OU) called "_EMPLOYEES"
- Create a new OU named “_ADMINS”
- Create a new employee named “Jane Doe” (same password) with the username of “jane_admin”
- Add jane_admin to the “Domain Admins” Security Group
- Log out/close the Remote Desktop connection to DC-1 and log back in as “cesarsdomain.com\jane_admin”
- User jane_admin as your admin account from now on


<h2>Configuration Steps</h2>

<p>
<h3>Step 1</h3>
After you have remote into the Windows Server VM, open up the Server Manager and click on Tools and then Active Directory Users and Computers.
</p>
<p>
<img src="https://i.imgur.com/7kxCz7J.png" height="80%" width="80%" alt="Configuration"/>
</p>

<p>
<h3>Step 2</h3>
Next we will create Organazation Units. In plain speak, they are similar to Folders. There are much more use cases for this but this is just an example. We are going to create two OU. One named "_EMPLOYEES" and the other named "_ADMINS". We can do this by right clicking on the domain name you created > New > Organizational Unit. 
</p>
<p>
<img src="https://i.imgur.com/5eFl4gN.png" height="80%" width="80%" />

