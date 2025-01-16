<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Create resouce groups and VM's in Azure
- Set dc-1 NIC pivate IP to Static
- Login into dc-1 and turn off Firewall
- Set Client1 to dc-1 private IP address

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="ResourceGroup.png" height="80%" width="80%" 
</p>
<p>
Create Resource group,Virtual network, and 2 VM's. 
</p>
<br />

<p>
<img src="StaticIP.png" height="80%" width="80%" 
</p>
<p>
Set dc-1 nic private ip address to static. You will click dc-1 in virtual machines, go to network settings, click the NIC, and at the bottom of the screen click ipconfig1 and press static under private ip address settings and Save.
</p>
<br />

<p>
<img src="VirtualMachines.png" height="80%" width="80%" 
</p>
<p>
Log into dc-1 by going to virtual machines, and copy the ip address to remote desktop and login. Right click Start and select run and type wf.msc. Select properties and turn off Firewall state under Domain profile, Private profile, and Public profile and press apply then ok.
</p>
<br />
<p>
<img src="DNS.png" height="80%" width="80%"
</p>
<p>
Set Client1 DNS settings to dc-1 private ip address to join the domain
</p>
<br />
