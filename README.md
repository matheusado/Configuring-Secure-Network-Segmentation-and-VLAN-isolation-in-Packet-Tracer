<h1>Secure-Network-Segmentation-VLAN-Isolation</h1>


<h2>Description</h2>
This project demonstrates the configuration of a segmented network in Cisco Packet Tracer, featuring a 14-node network and a 6-node network with VLAN-isolated web servers. All devices are manually configured using static IP addressing to ensure precise control over network communication. The setup includes router and switch configuration, VLAN segmentation for isolation, and inter-network connectivity to enable secure and efficient communication.
<br />


<h2>Languages and Utilities Used</h2>

- Cisco Packet Tracer – Used for designing and simulating the entire network topology.
- Static IP Configuration – Manually assigned IP addresses to all nodes for precise control and segmentation.
- Cisco IOS CLI – Utilized for configuring routers and switches through command-line interface commands.
- Networking Concepts – Applied IP addressing, subnetting, VLAN segmentation, inter-VLAN routing, and basic switching techniques.

<h2>Environments Used </h2>

- <b>macOS Ventura 13.7.4</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
Launch Cisco Packet Tracer: <br/>
<img src="https://i.imgur.com/ZRUAO4Y.png"/>
<br />
<br />
Select 2960-24TT switch and drag it to the main screen:  <br/>
<img src="https://i.imgur.com/Th4ubMg.png"/>
<br />
<br />
Select PC-PT and drag 12 computers to the main screen: <br/>
<img src="https://i.imgur.com/FiWKQGF.png"/>
<br />
<br />
Select the Copper Straight-Through cable, connect the computers to the switch using FastEthernet0 port on them and different ports in the switch:  <br/>
<img src="https://i.imgur.com/hNpFZcK.png"/>
<br />
<br />
Setting up a 6-node network, drag a switch and  5 computers, connect them using Copper Straight-Through cable, using FastEthernet0 port on the computers and  choose different ports in the switch :  <br/>
<img src="https://i.imgur.com/myzZrDo.png"/>
<br />
<br />
Click on Routers, select 2621XM Router and drag it to the main screen:  <br/>
<img src="https://i.imgur.com/6aiFhS0.png"/>
<br />
<br />
Using Copper Straight-Through cable, connect the router to the switches using different ports:  <br/>
<img src="https://i.imgur.com/SbdcUtw.png"/>
<br />
<br />
Click on End Devices, select a Server, drag it to the main screen and connect it to the Switch of the left side using a Copper Straigh-Through cable, using FastEthernet port on the Server and a different port on the Switch:  <br/>
<img src="https://i.imgur.com/uI4dk48.png"/>
<br />
<br />
In the browser, paste the link given below and press enter:
https://www.calculator.net/ip-subnet-calculator.html:  <br/>
<img src="https://i.imgur.com/Xz1SKAg.png"/> 
<br />
<br />
Select 255.255.255.240/28 as Subnet and 192.168.110.0 as IP Address:  <br/>
<img src="https://i.imgur.com/EHohnJD.png"/>
<br />
<br />
Click on Calculate and review the Usable Host IP Range, Number of Usable Hosts, and Subnet Mask from the output:  <br/>
<img src="https://i.imgur.com/7xx4PLM.png"/>
<br />
<br />
Navigate back to Packet Tracer,click on Server0 and select Desktop:  <br/>
<img src="https://i.imgur.com/zl9uzCY.png"/>
<br />
<br />
Click on IP Configuration:  <br/>
<img src="https://i.imgur.com/6J9Y0Kw.png"/>
<br />
<br />
Select Static and enter 192.168.110.1 as the IP Address, enter 255.255.255.240 as Subnet Mask and 192.168.110.14 as Default Gateway:  <br/>
<img src="https://i.imgur.com/adSkQKs.png"/>
<br />
<br />
Select Services tab and click on DHCP:  <br/>
<img src="https://i.imgur.com/39qMukf.png"/>
<br />
<br />
Turn DHCP on, enter Pool001 as Pool Name, 192.168.110.14 as Default Gateway, 192.168.110.2 as Start IP Address, 255.255.255.240 as Subnet Mask then enter 14 as Maximum number of Users and click add: <br/>
<img src="https://i.imgur.com/72slbDo.png"/>
<br />
<br />
Navigate back to the main screen and click on PC0, select Desktop then IP Configuration, select Static and add 192.168.110.2 as the IP address and 255.255.255.240 as Subnet Mask:<br/>
<img src="https://i.imgur.com/0vUwiJK.png"/>
<br />
<br />
Repeat the same steps for the remaining 11 PCs (PC1 – PC11), choosing the subsequent IP addresses from 192.168.110.3 to 192.168.110.13:  <br/>
<img src="https://i.imgur.com/sMbDENh.png"/>
<br />
<br />
Click on the Router, select Config, click at FastEthernet0/0 on the Interface tab, add 192.168.110.14 as the IP Address, 255.255.255.240 as the Subnet mask and turn on the Port Status: <br/>
<img src="https://i.imgur.com/OjOsNBf.png"/>
<br />
<br />
In the browser, paste the link given below and press enter:
https://www.calculator.net/ip-subnet-calculator.html: <br/>
<img src="https://i.imgur.com/Xz1SKAg.png"/>
<br />
<br />
Select 255.255.255.248/29 as Subnet, enter 192.168.120.0 as IP Address and click in Calculate: <br/>
<img src="https://i.imgur.com/Hxf8Pv0.png"/>
<br />
<br />
Review the Usable Host IP Range, Number of Usable Hosts, and Subnet Mask from the output: <br/>
<img src="https://i.imgur.com/kIQDiZY.png"/>
<br />
<br />
Navigate back to Packet Tracer, click on PC12, select Desktop, IP configuration, click in Static and enter 192.168.120.1 as the IP Address, 255.255.255.248 as Subnet Mask and 192.168.120.6 as Default Gateway: <br/>
<img src="https://i.imgur.com/UjjWUe1.png"/>
<br />
<br />
Repeat the same steps for the remaining 4 PCs (PC13 – PC16), choosing the subsequent IP addresses from 192.168.120.2 to 192.168.120.5: <br/>
<img src="https://i.imgur.com/WmnZZTF.png"/>
<br />
<br />
To check connectivity, click on PC1, select Desktop then Command Prompt, run the code ping 192.168.110.3 and tracert 192.168.120.3: <br/>
<img src="https://i.imgur.com/SY4Aea6.png"/>
<br />
<br />
Click on PC12, select Desktop then Command Prompt, run the code ping 192.168.120.2 and tracert 192.168.110.4: <br/>
<img src="https://i.imgur.com/UMbN6tw.png"/>
<br />
<br />
Click on the Switch, select Config then Vlan Database, enter 10 in VLAN Number and Web-Server-RnD in VLAN Name then click add, you can also do it on CLI tab running the command vlan 10 and name Web-Server-Rnd: <br/>
<img src="https://i.imgur.com/dWjT5qV.png"/>
<img src="https://i.imgur.com/Opu0b1N.png"/>
<br />
<br />
Navigate to FastEthernet0/1 and select 10 in the VLAN field: <br/>
<img src="https://i.imgur.com/KAHBeNY.png"/>
<br />
<br />
Navigate to FastEthernet0/2 and select 10 in the VLAN field: <br/>
<img src="https://i.imgur.com/5IzHKCw.png"/>
<br />
<br />
Click on PC12, select Desktop then Command Prompt, Run the following command: ping 192.168.120.2 <br/>
<img src="https://i.imgur.com/10yxK3H.png"/>
Note: Both are in the same VLAN, allowing them to ping each other.
<br />
<br />
Run the following command: ping 192.168.110.3: <br/>
<img src="https://i.imgur.com/vKojDvP.png"/>
Note: They are in different VLANs, so they will not be able to ping each other.
<br />
<br />
By following the above steps, you have successfully configured a secure network segmentation and VLAN isolation in Cisco Packet Tracer. This process involved the setup of a 14-node network, a 6-node network, and the integration of both networks using a router to ensure seamless communication. <br/>
<img src="https://i.imgur.com/d3nT33M.png"/>
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
