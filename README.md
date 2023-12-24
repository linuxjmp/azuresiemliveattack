<h1>Azure SIEM Live Attack</h1>

<h2>Description</h2>
Create an advanced cybersecurity monitoring solution leveraging Azure Sentinel (SIEM) integrated with a strategically deployed honeypot VM. This setup is specifically designed to track and analyze RDP brute force attacks on a global scale. The project features a bespoke PowerShell script, crafted for real-time geolocation tracking of attackers. It showcases an innovative use of Azure Sentinel's mapping capabilities, enabling advanced visualization and threat analysis. This project demonstrates a practical application of SIEM tools in identifying and visualizing cyber threats in a dynamic, real-world context.
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
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Azure SIEM Live Attack Steps"/>
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
