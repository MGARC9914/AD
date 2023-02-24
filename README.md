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

<h2>Install Active Directory</h2>

- Install both Windows Server and Windows 10 VMs.
<img src="https://i.imgur.com/2M7SwNl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/vPWYTgU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

- On the Windows Server virtual machine you will have server manager open up.
 <img src="https://i.imgur.com/V5HJKit.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

- In server manger click on "Add roles and features" to install Active directory into the virtual machine.
<img src="https://i.imgur.com/62Rw3ft.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/DBpP26p.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/GySGG9Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 
- Now Active Directory should appear in server mmanger after restarting the VM.
<img src="https://i.imgur.com/p9T5RnS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>







<h2>Deployment and Configuration Steps</h2>

<p>
<li> Before we continue we got to make sure that our Windows Server vm private IP address is set to static.</li>
</p>
<p>
<img src= "https://i.imgur.com/BAS9UuY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<li> Next on the "Active Directory Domain Services Configuration Wizard" we are creating our domain.</li>
</p>
<p>
<img src= "https://i.imgur.com/5Mw43sX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src= "https://i.imgur.com/hC8CSjh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<li> Now that the Windows Server vm has its own DNS server we need to connect the windows 10 vm(client-1) through Azure.</li>
</p>
<p>
<img src= "https://i.imgur.com/5SuboEt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src= "https://i.imgur.com/fCm9aVV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<li> Since Windows 10 vm is connected to the Windows Server vm DNS server now we can connect client 1 vm to the dommain we created earlier(mydomain.com).</li>
</p>
<p>
<li> First we  go to Settings->About->Rename the PC(advanced).</li>
</p>
<p>
<img src= "https://i.imgur.com/0MWXftA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<li> Then click on "Change...". After click Domain and type in the domain we created earlier which was domain.com. The click "ok" when finished.</li>
</p>
<p>
<img src= "https://i.imgur.com/ujtHqly.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src= "https://i.imgur.com/DV6voSL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />

