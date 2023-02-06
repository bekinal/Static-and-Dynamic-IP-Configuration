<h1>Static & Dynamic IP Configuration</h1>

<h2>Description</h2>
Project consists of setting up a static IP address confiugration to learn about system network services.
<br />


<h2>Utilities Used</h2>

- <b>VirtualBox</b>
- <b>Debian Environment</b>
- <b>Terminal</b>

<h2>Making an IP Address Static:</h2>
Terminal is opened and a root user is accessed:<br/>
<img src="https://imagizer.imageshack.com/img922/434/1PHw9Q.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The ip address command is used to identify the name of the NIC and IP address allocated to it:<br/>
<img src="https://imagizer.imageshack.com/img924/966/9drVAm.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The ip route command shows the address of the default gateway:<br/>
<img src="https://imagizer.imageshack.com/img924/907/NjnnBo.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The touch command is used to create a file named enp0s3 in the interfaces.d directory:<br/>
<img src="https://imagizer.imageshack.com/img923/1226/RKeWgp.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The file is then opened with nano:<br/>
<img src="https://imagizer.imageshack.com/img922/6237/asgn9h.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The following data is enterted to configure a static IP. It can be noted that the IP address is on the same subnet as the current IP:<br/>
<img src="https://imagizer.imageshack.com/img924/6139/NpxFhX.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The file is then saved, and exited:<br/>
<img src="https://imagizer.imageshack.com/img924/7800/ajxVk9.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The networking stop comand is used to stop the networking service:<br/>
<img src="https://imagizer.imageshack.com/img922/7199/8cXkHT.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The networking manager restart command is used to restart the network manager service:<br/>
<img src="https://imagizer.imageshack.com/img924/8697/gYpoRW.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The networking start command is used to start the networking service:<br/>
<img src="https://imagizer.imageshack.com/img924/7347/9t9SCF.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The ip address command is used to confirm that the static IP address was configured properly:<br/>
<img src="https://imagizer.imageshack.com/img923/5086/CpuBtu.png" alt="Disk Sanitization Steps"/>
<br />
<br />
A ping to google's DNS confirms communication from the host to the world:<br/>
<img src="https://imagizer.imageshack.com/img924/8536/1778Qm.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The "rm" command is used to remove the enp0s3 file. The machine is then restarted to recieve a DHCP IP:<br/>
<img src="https://imagizer.imageshack.com/img922/664/LhTQGp.png" alt="Disk Sanitization Steps"/>
<br />
<br />


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
