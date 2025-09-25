<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1: Install Active Directory
- Step 2: Create a Domain Admin user within the domain
- Step 3:  Join Client-1 to your domain (mydomain.com)

<h2>Deployment and Configuration Steps</h2>
Install Active Directory
—
Login to DC-1 and install Active Directory Domain Services

Promote as a DC: Setup a new forest as mydomain.com (can be anything, just remember what it is)

Restart and then log back into DC-1 as user: mydomain.com\labuser

<img width="1429" height="745" alt="image" src="https://github.com/user-attachments/assets/484c87ee-7858-4d28-ab01-4cec5d6e0be3" />
<img width="784" height="559" alt="image" src="https://github.com/user-attachments/assets/d082aafe-95d6-4239-ab1a-28e967a00c0b" />
<img width="1426" height="715" alt="image" src="https://github.com/user-attachments/assets/2daede61-f0bd-4663-adbf-696e4558e555" />

Create a Domain Admin user within the domain
—
In Active Directory Users and Computers (ADUC), create an Organizational Unit (OU) called “_EMPLOYEES”

Create a new OU named “_ADMINS”

Create a new employee named “Jane Doe” (same password) with the username of “jane_admin” / Cyberlab123!

Add jane_admin to the “Domain Admins” Security Group

Log out / close the connection to DC-1 and log back in as “mydomain.com\jane_admin”
User jane_admin as your admin account from now on

<img width="757" height="526" alt="image" src="https://github.com/user-attachments/assets/90cf1437-f6b6-4447-bfe3-342681a45c2d" />
<img width="1837" height="877" alt="image" src="https://github.com/user-attachments/assets/e555d2d0-608e-4cdf-9315-839d1ec49b90" />

Login to Client-1 as the original local admin (labuser) and join it to the domain (computer will restart)

Login to the Domain Controller and verify Client-1 shows up in ADUC

Create a new OU named “_CLIENTS” and drag Client-1 into there

<img width="490" height="241" alt="image" src="https://github.com/user-attachments/assets/b1c28451-f5e8-477f-90ea-ebb7f80e7790" />
<img width="760" height="538" alt="image" src="https://github.com/user-attachments/assets/e7933a61-4b84-4b86-a298-695445b193a5" />
<img width="763" height="538" alt="image" src="https://github.com/user-attachments/assets/af4ad714-a94a-4131-ad9a-133538366bb8" />







<p>
</p>
<p>

</p>
<br />

<p>

</p>
<p>

</p>
<br />

<p>

</p>
<p>

</p>
<br />
