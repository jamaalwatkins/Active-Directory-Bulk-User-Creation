# Active Directory Bulk User Creation





<h2>Description</h2>
<b>The Powershell script is responsible for creating 1000 user accounts in active diretory.  The script takes sample names and places them into an array.  While creating a new USERS organizational unit. 
</b>
<br />
<br />
The script is used in this demo where I setup an Active Directory on my computer using virtualbox.  
Virtualbox will be the machine used. Installing Server 2019 ISO on one virtual machine and Windows 10 ISO on another.  Server virtual machine will be the Domain Controller housing active directory. Domain controller will have two netowrk adapters (NIC) one network used to connect to the outside internet and the other network used to connect to a private virtualbox internet for clients to use.  The private network will be assigned an IP address.  Domain Controller will get have active directory installed and domain created.  Then configure RAS & NAT for private network so clients can reach the internet through the domain controller. Set up a DHCP on the domain controller so clinet machine can automatically get an IP address. Run powershell script to automatically create users in active directory.    
<br />
<br />
Create private client (Client 1) on Windows 10 virtual machine to connect to private virtual box network and log in with active directory user (Domain Account).
<br />
<br />
<p align="center">
<img src="https://imgur.com/pPHqVsy.png" height="85%" width="85%" alt="RDP event fail logs to iP Geographic information"/>
</p>
<h2>Languages Used</h2>

- <b>PowerShell:</b> Create user accounts 

<h2>Utilities Used</h2>

- <b>Virtualbox<br/>
- <b>Windows ISO 10 Pro<br/>
- <b>Server 2019 ISO


<h2>Set Up Two Virtual Machines and Configure Settings</h2>

<p align="center">
<img src="https://imgur.com/bCi03F4.jpeg" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<h2>Assign IP Address for Internal Network</h2>

<p align="center">
<img src="https://imgur.com/glBuliZ.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<h2>Install Active Directory Domain Services and Create Domain</h2>

<p align="center">
<img src="https://imgur.com/xmLxtJU.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>
 
 <p align="center">
 <h2>Configure Remote Access Server (RAS) & Network Address Translation (NAT) </h2>
 
 <p align="center">
         <h3>Allows internal clients to connect to the internet using one public IP address.<h3><br/>
</p>
<p align="center">
<img src="https://imgur.com/Sm4nIMq.png" height="85%" width="85%"</h2>

 </p>
<p align="center">
<h2>Set Up DHCP Server on Domain Controller</h2>
<h3>Allows Windows 10 Clients to get a IP Address for Private Internet<h3><br/>
<p align="center">
<img src="https://imgur.com/uJH53ps.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>
 
 <p align="center">
<h2>Run Powershell Script to Import Active Directory Users</h2>

<p align="center">
<img src="https://imgur.com/lrZhHwJ.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

 <p align="center">
<h2>Create Windows 10 Client and Setup Internal NIC</h2>

<p align="center">
<img src="https://imgur.com/Juo43ms.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>
 
 <p align="center">
<h2>Create Windows 10 Client and Setup Internal NIC</h2>

<p align="center">
<img src="https://imgur.com/Juo43ms.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>
 
 <p align="center">
<h2>Confirm Client Windows 10 Machine has Access to Domain Controller Internal Internet</h2>

<p align="center">
<img src="https://imgur.com/1r972MP.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>
 
 <p align="center">
<h2>Join Domain Network</h2>

<p align="center">
<img src="https://imgur.com/1r972MP.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>
