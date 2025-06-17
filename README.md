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

- Step 1 Provision Azure Virtual Machines
- Step 2 Install Active Directory Domain Services
- Step 3 Promote Server to Domain Controller
- Step 4 Join Client to Domain and Test

<h2>Deployment and Configuration Steps</h2>


![1D9DEF7E-7A1F-41F7-9640-6D599B9E1B80](https://github.com/user-attachments/assets/917b761b-1632-41f1-91c5-dbd38b1d2beb)
</p>
<p>
Step 1: Provision Azure Virtual Machines
Create two virtual machines using Windows Server 2022 (one for AD DS, another as a secondary server or client test machine).
Ensure both VMs are in the same virtual network and subnet.
<p>
Step 2: Install Active Directory Domain Services
Log into the primary VM using Remote Desktop.
Use Server Manager to install the Active Directory Domain Services (AD DS) role.
</p>
<br />

![C81C8FD9-803D-4338-B2AB-4161717613E1](https://github.com/user-attachments/assets/d3cc9fc3-1e59-4041-b343-83667091ac68)


</p>
<p>
Step 3: Promote Server to Domain Controller
After installing AD DS, promote the server to a Domain Controller.
Create a new forest (e.g., corp.local) and configure DNS during this process.
Restart the VM to finalize the domain configuration.
<p>
Step 4: Join Client to Domain and Test
Use the second VM (e.g., Windows 10) to join the newly created domain.
Verify connectivity, login using a domain account, and test group policies or user management from Active Directory Users and Computers.
</p>
<br />

![9CFB0E7D-6677-4B2E-8E3B-BDB79F7C7AF1](https://github.com/user-attachments/assets/7002f78a-61fc-4321-b4f7-fc3af0a22d47)

</p>
<p>
Deployment and Configuration

Set Up Azure Resource Group and Virtual Network
Use Azure Portal or PowerShell to create a resource group and virtual network with necessary subnets.

Deploy VMs
Deploy at least one Windows Server 2022 VM and one Windows 10 VM in the same subnet.
Configure VM Networking

Assign static private IPs and enable RDP access through NSG rules.
Install and Configure AD DS

Install AD DS on the Server VM.
Promote the VM to a domain controller and configure DNS.
Test domain join and domain-based authentication on the client machine.
</p>
<br />
