<h1>Azure SIEM Live Attack</h1>

<h2>Description</h2>
Create an advanced cybersecurity monitoring solution using Azure Sentinel (SIEM) integrated with a honeypot VM. This setup is specifically designed to track and analyze RDP brute force attacks on a global scale. The project features a custom PowerShell script, crafted for real-time geolocation tracking of attackers. It showcases an innovative use of Azure Sentinel's mapping capabilities, enabling advanced visualization and threat analysis. This project demonstrates a practical application of SIEM tools in identifying and visualizing cyber threats in a dynamic, real-world context.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Azure Sentinel</b>
- <b>ipgeolocation.io </b> (API)
- <b>PowerShell</b>
- <b>Kusto Query Language (KQL)</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)
- <b>Azure</b> 

<h2>Project walk-through:</h2>

<p align="center">
Create a virtual machine (VM): <br/>
<img src="https://imgur.com/jErEKir.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
<b>Create a new inbound network security rule to allow all traffic:<b/>
  <br/>
  <img src="https://i.imgur.com/qer2KAS.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps" />
  <br/>
  <br/>
  <img src="https://i.imgur.com/2OX6ZN6.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps" />
<br />
<br />
  <img src="https://i.imgur.com/xtPncQW.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps" />
  <br />
  <br />
Create a log analytics workspace: <br/>
<img src="https://i.imgur.com/WbbG2q3.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
Enable gathering logs in MS Defender for cloud:  <br/>
<img src="https://i.imgur.com/ypjCVRX.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
<img src="https://i.imgur.com/ypjCVRX.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
<img src="https://i.imgur.com/ZgctLvu.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
<img src="https://i.imgur.com/F5x0NLs.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
<img src="https://i.imgur.com/PSwG9bS.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br /> 
<img src="https://i.imgur.com/OdI2iw4.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
Setup Azure Sentinel: <br />
<img src="https://i.imgur.com/pfrqWpX.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br /> 
<br /> 
<img src="https://i.imgur.com/v4Rg886.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
Find the virtual machine IP address and log in via RDP:  <br/>
<img src="https://i.imgur.com/jRqclxw.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
Open Windows Defender Firewall and turn off the firewall: <br/>
<img src="https://i.imgur.com/xV1p5l7.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
<img src="https://i.imgur.com/OXTaEMA.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
Copy & paste the custom PowerShell script & put it into Powershell ISE: <br/>
<img src="https://i.imgur.com/Q3nr5Td.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
Get your API from ipgeolocation.io: <br/>
<img src="https://i.imgur.com/H39EWif.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
Replace API key variable with your API key in Powershell ISE: <br/>
<img src="https://i.imgur.com/E6GchVx.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
Run the script to gather IP geo data from attackers: <br/>
<img src="https://i.imgur.com/Eq3uIKC.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/
<br />
<br />
Copy sample log created by Powershell Script in VM to host machine from C:\ProgramData\failed_rdp.log: <br/>
<img src="https://i.imgur.com/VnzFD6E.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
<img src="https://i.imgur.com/bZtWzQT.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
Create a custom MMA-based log in LAW to bring in our custom log: <br/>
<img src="https://i.imgur.com/uoSBHxU.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
Upload sample log to train Defender on the format of logs: <br/>
<img src="https://i.imgur.com/ZgVIrcw.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
<img src="https://i.imgur.com/SX3nKrl.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
Set the collection path of log to its location in the VM: <br/>
<img src="https://i.imgur.com/zNU5EoV.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
Name and create: <br/>
<img src="https://i.imgur.com/AWyqHy0.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
Wait a couple of hours for attackers to find the VM & run custom KQL query to test if working: <br/>
<img src="https://i.imgur.com/XGzYBG9.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
Create a new workbook in Microsoft Sentinel & delete sample sections:  <br/>
<img src="https://i.imgur.com/ab23hos.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
Run custom KQL query in Microsoft Sentinel: <br/>
<img src="https://i.imgur.com/rgFn8Om.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
Change visualization setting to map: <br/>
<img src="https://i.imgur.com/lfnUbkX.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
<img src="https://i.imgur.com/9Zt8Wlb.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
Adjust settings to show location data of your interest: <br/>
<img src="https://i.imgur.com/HQskFaJ.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
<br />
<br />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
