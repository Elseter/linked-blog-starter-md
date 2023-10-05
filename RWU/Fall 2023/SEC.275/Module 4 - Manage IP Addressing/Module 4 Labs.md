---
aliases:
  - "20230925170316"
tags:
  - SEC
  - SEC275
  - TestOutServer
date_created: 2023-09-25 17:03
Index: "[[SEC.275 Index]]"
---
# Module 4 Labs
---
## 4.1.11 - Configure IP Addresses
### Prompt
You work as the IT administrator for a small corporate network. You need to configure the workstation in the executive office so it can connect to the local network and the internet. The workstation has two network interface cards (named Ethernet and Ethernet 2). Having two network cards allows the workstation to connect to the local network (as shown in the exhibits) and another small network, which is not yet built.

In this lab, your task is to:

- For both network cards, configure the IP version 4 TCP/IP settings using the settings specified in the table below.
- From the Exec computer, ping the preferred DNS server assigned to the Ethernet NIC to verify that it can communicate successfully.

|                              |                                                                         |                                                       |
| ---------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------- |
| TCP/IP Setting  <br>or Info  | Ethernet                                                                | Ethernet 2                                            |
| Subnet                       | 192.168.0.0/24                                                          | 10.0.0.0/16                                           |
| IP address                   | Use the last valid address on the subnet.                               | Use the last valid address on the subnet.             |
| Subnet mask                  | Use the default mask that matches the Class C subnet.                   | Use the default mask that matches the Class B subnet. |
| Default gateway              | Choose the appropriate address for the router as shown in the exhibits. | Do not configure a default gateway value.             |
| Preferred DNS server address | Use the address of an external DNS server as shown in the exhibits.     | Do not configure a DNS value.                         |
| Alternate DNS server address | Use the address of an external DNS server as shown in the exhibits.     | Do not configure a DNS value.                         |
### Answer
![[Screenshot 2023-09-25 at 5.57.17 PM.png]]
![[Screenshot 2023-09-25 at 5.57.33 PM.png]]

---
## 4.2.4 Explore IP Configuration
### Prompt
You are a network technician for a small corporate network. The network is connected to the internet and uses DHCP for address assignment. Employees in Office 1 and the Executive Office are reporting problems with their network connections.

In this lab, your task is to explore, diagnose, and fix the reported TCP/IP configuration problems.

Use the following troubleshooting tools:

- The **ping**, **ipconfig**, or **tracert** command utilities
- The Network and Sharing Center in the Windows 10 or Windows 2022 operating system
- The DHCP server console in the Windows 2019 operating system
- The network diagram/schematic as found in Exhibits

Complete this lab as follows:

1. From CorpServer, mouse over the network icon in the Notification Area.  
    Notice that the Notification Area appears normal (a computer icon is shown), which indicates a connection to the local network and the internet. When you mouse over the network icon, you see the details of this status.
2. Access the Network Connections window.
    1. Right-click **Start** and then select **Settings**.
    2. Select **Network & Internet**.  
        The Settings Status diagram confirms that CorpServer is connected to the local network and to the internet.
    3. Close the Settings app.
3. Ping the ISP to verify connectivity through the router and the internet.
    1. From the top right, select **Exhibits**.
    2. Locate the IP address of the ISP.
    3. From the top right, select **Answer Questions.**
    4. Answer Question 1.
    5. Close the Exhibits window.
    6. Right-click **Start** and select **Windows PowerShell (Admin)**.
    7. From the PowerShell prompt, type **ping _ISP_IPaddress_** and press **Enter**.  
        Notice that the ping was successful, verifying a valid connection to the internet.
4. Use the **ipconfig** and **tracert** commands to find the devices used to access the ISP.
    1. From the PowerShell prompt, type **ipconfig /all** and press **Enter**.
    2. Locate and examine the **vEthernet (External)** configuration settings and note the following:
        - DHCP Enabled: **No**  
            This tells us that the server is configured with a static IP address and is not enabled for DHCP.
        - IPv4 Address: **192.168.0.10**
        - Subnet Mask: **255.255.255.0**  
            The server is using the default subnet mask for the Class C IP address range.
        - Default Gateway: **192.168.0.5**  
            The router's internal interface is configured as the default gateway.
    3. From the PowerShell prompt, type **tracert _ISP_IPaddress_** to see the path to the ISP.
    4. Answer Question 2.
    5. From the top right, select **Exhibits**.
    6. Answer Question 3.
    7. Minimize the Lab Questions window.
    8. Close the Exhibits window.
5. From the Executive Office, check the status of the link and network activity lights.
    1. From the top left, select **Floor 1 Overview**.
    2. Under _Executive Office_, select **Hardware**.
    3. Above the workstation, select **Back** to switch to the back view of the workstation.  
        The link and network activity lights on the network card are on and blinking. This indicates that there is a physical connection to the switch and there is activity on the connection. This points to a TCP/IP configuration problem.
6. Verify the connectivity on the Exec workstation.
    1. On the Exec monitor, select **Click to view Windows 10**.
    2. In the Notification Area, mouse over the **network** icon.  
        Notice that the pop-up indicates there is no internet access.
    3. Right-click **Start** and then select **Settings**.
    4. Select **Network & Internet**.  
        The Network Status diagram confirms that the Exec computer has no connection to the internet.
    5. Close the Settings app.
    6. Right-click **Start** and select **Windows PowerShell (Admin)**.
    7. From the PowerShell prompt, type **ping Exec** and press **Enter**.  
        Notice that the ping was successful.
    8. From the PowerShell prompt, type **ping CorpServer** and press **Enter**.  
        Notice that the ping to CorpServer failed.
    9. From the PowerShell prompt, type **ipconfig /all** and then press **Enter**. From this command, the following is shown for the Ethernet interface card:
        
        - DHCP Enabled: **No**
        - IPv4 Address: **192.168.0.62**
        - Subnet Mask: **255.255.255.240**
        - Default Gateway: **192.168.0.4**
        
        This information provides the following clues to the problem:
        
        - The network is using DHCP, but this workstation is not enabled for DHCP.
        - Given the workstation's current subnet mask, the IPv4 address of the workstation and the default gateway are not on the same network.
        - The subnet mask is not the default subnet mask for the Class C IP address range being used. With 255.255.255.240 as a subnet mask, the network would only include addresses from 192.168.0.48 to 192.168.0.63.
        - In Step 4, you learned that CorpServer (192.168.0.10) had a default subnet mask for the Class C IP address range (255.255.255.0), which doesn't match Exec.
7. Fix the subnet mask for the Exec computer.
    1. Right-click **Start** and then select **Settings**.
    2. Select **Network & Internet**.
    3. From the left pane, select **Ethernet**.
    4. From the right pane, select **Change adapter options**.
    5. Right-click **Ethernet** and select **Properties**.
    6. Select **Internet Protocol Version 4 (TCP/IPv4)** and then select **Properties**.
    7. Change the Subnet mask to **255.255.255.0** and then select **OK**.
    8. From the PowerShell prompt, type **ping CorpServer** and then press **Enter**.  
        Notice that the ping is successful.
    9. From the PowerShell prompt, type **ping 198.28.2.254** (the ISP) and then press **Enter**.  
        Notice that the ping is unsuccessful.
    10. From the PowerShell prompt, type **tracert 198.28.2.254** (the ISP) and then press **Enter**.  
        The command times out, indicating that the gateway address on Exec is not configured correctly. The gateway address (router) on the network diagram is 192.168.0.5.
8. Fix the default gateway for the Exec computer.
    1. From the Ethernet Properties dialog, select **Internet Protocol Version 4 (TCP/IPv4)** and then select **Properties**.
    2. Change the Default gateway to **192.168.0.5**
    3. Select **OK** and then select **Close**.
    4. Close the Network Connections window.
    5. From the Settings app, select **Status**.  
        The Status pane now shows a connection to the internet.
    6. Close the Settings app.  
        Notice that the network icon in the Notification Area is now showing a computer, indicating a connection to the internet.
    7. Type **ping 198.28.2.254** from the PowerShell prompt.  
        The ping is now successful.
    8. From the PowerShell prompt, type **tracert 198.28.2.254** and press **Enter**.  
        The route taken to get to the ISP is now shown.  
        Since there is now a valid connection to the internet, leave the static address for now and begin to troubleshoot the computer in Office 1.
9. From Office 1, troubleshoot for network connectivity.
    
    1. From the top left, select **Floor 1 Overview**.
    2. Under Office 1, select **Hardware**.
    3. Above the workstation, select **Back** to switch to the back view of the workstation.  
        The link and network activity lights on the back of the workstation are on and blinking, indicating that there is a physical connection to the switch and there is activity on the connection. Once again, this points to a TCP/IP configuration problem.
    4. On the Office1 monitor, select **Click to view Windows 10**.
    5. In the Notification Area, mouse over the **network** icon.  
        Notice that the pop-up indicates there is no internet access.
    6. Right-click **Start** and select **Windows PowerShell (Admin)**.
    7. From the PowerShell prompt, type **ipconfig /all** and then press **Enter**.  
        Examine the information for the Ethernet network card and note the following:
    
    - DHCP Enabled: **Yes**  
        This tells us that the workstation is configured to use a DHCP server.
    - IPv4 Address: This address is in the APIPA range (169.254.0.1 to 169.254.255.254). This means that the workstation assigned itself an IP address instead of receiving one from the DHCP server. The workstation will only be able to communicate with other hosts on the local network that have also configured their own IP address through APIPA.
    - Subnet Mask: 255.255.0.0. This is the default subnet mask for the APIPA address.
    - Default Gateway: The address is blank. This means that communication is limited only to other workstations on the local network.
    - DHCP Server line is not shown. This means that the workstation was unable to contact the DHCP server.
    - DNS Servers line is not shown for IPv4.  
        Since DHCP is enabled, the rest of the information should have come from the DHCP server. From this, you can conclude that there is an issue with the DHCP server.
10. From CorpServer, access the CorpDHCP server.
    1. From the top left, select **Floor 1 Overview**.
    2. Under Networking Closet, select **CorpServer**.
    3. From the Hyper-V Manager, select **CORPSERVER**.
    4. Maximize the window for better viewing.
    5. Double-click **CorpDHCP** to connect to the CorpDHCP virtual server.
11. From CorpDHCP, launch the DHCP console and activate the scope.
    1. From CorpDHCP's menu bar, select **Tools** > **DHCP**.
    2. Expand **CorpDHCP.CorpNet.local** > **IPv4**.  
        Notice that the folder icon for _Scope [192.168.0.1] Subnet1_ has a down arrow, indicating that the DHCP scope is not active.
    3. Right-click **Scope [192.168.0.1] Subnet1** and select **Activate**.
12. From Office1, check to see if activating DHCP fixed the issue.
    1. From the top left, select **Floor 1 Overview**.
    2. Under Office 1, select **Office1**.
    3. From the PowerShell prompt, type **ipconfig /renew** and press **Enter**. This command requests new IP address information from the DHCP server.  
        Notice that the networking icon in the Notification Area still indicates that Office1 has no connection to the internet.
    4. From the PowerShell prompt, type **ipconfig /all** and press **Enter**.  
        Notice the line for the default gateway, DNS server, and DHCP server (along with the new IP address) is now within the DHCP scope for the local network.
    5. From the PowerShell prompt, type **ping CorpServer** and press **Enter**.The ping command is successful.
    6. From the PowerShell prompt, type **ping 198.28.2.254** (the ISP) and then press **Enter**.  
        Although you can ping CorpServer, you are still unable to ping the ISP.
    7. Review the output from the ipconfig command.  
        Notice that the default gateway does not match the default gateway used by CorpServer or Exec. Since this IP information is coming from the DHCP server, you need to check the DHCP scope.
13. On CorpServer, from CorpDHCP, reconfigure the settings for the DHCP scope.
    1. From the top left, select **Floor 1 Overview**.
    2. Under Networking Closet, select **CorpServer**.
    3. From the DHCP console, expand **Scope [192.168.0.1] Subnet1**.
    4. Right-click **Scope Options** and then select **Configure Options**.
    5. Highlight the **003 Router** line.
    6. Under IP address, select **192.168.0.2** and then click **Remove**.
    7. In the IP address field, change the address to **192.168.0.5** and then click **Add**.
    8. Select **OK**.
14. From Office1, check to see if fixing the DHCP scope resolved the issue.
    1. From the top left, select **Floor 1 Overview**.
    2. Under Office 1, select **Office1**.
    3. From the PowerShell prompt, type **ipconfig /renew** and then press **Enter**. This command requests new IP address information from the DHCP server.  
        Notice that the networking icon in the Notification Area now indicates that Office1 has a connection to the internet.
    4. From the PowerShell prompt, type **ipconfig /all** and then press **Enter**.  
        Notice the line for the default gateway is now set to 192.168.0.5.
    5. From the PowerShell prompt, type **ping 198.28.2.254** (the ISP) and then press **Enter**.  
        You can now ping the ISP.
15. On Exec, reconfigure the Ethernet connection to use DHCP.
    1. From the top left, select **Floor 1 Overview**.
    2. Under Executive Office, select **Exec**.
    3. Right-click **Start** and then select **Settings**.
    4. Select **Network & Internet**.
    5. Select **Ethernet** and then select **Change adapter options**.
    6. Right-click **Ethernet** and then select **Properties**.
    7. From the Ethernet Properties dialog, select **Internet Protocol Version 4 (TCP/IPv4)** and then click **Properties**.
    8. Select **Obtain an IP address automatically**.
    9. Select **Obtain DNS server address automatically**.
    10. Select **OK** and then select **Close**.
    11. From the PowerShell prompt, type **ipconfig /all** and then press **Enter**.  
        Notice that the Ethernet card is now using DHCP (DHCP Enable: Yes).
    12. From the PowerShell prompt, type **tracert 198.28.2.254** and then press **Enter**.  
        The command returns a path to the ISP through the gateway. The network is now fully functional, and your troubleshooting is complete.
16. Score the lab.
    1. From the top right, select **Answer Questions.**
    2. Select **Score Lab**.
### Answer
![[TestOut LabSim.pdf]]

---
## 4.2.5 - Troubleshoot IP Configuration 1
### Prompt
You are a network technician for a small corporate network. The network is connected to the internet and uses DHCP for address assignment. The employees in the IT Administration Office and Office 2 report that their workstations can communicate with some computers on the network but cannot access the internet. You need to diagnose and fix the problem. The following IP addresses are used in your network:

|   |   |
|---|---|
|Device|IP Address|
|CorpServer|192.168.0.10|
|ITAdmin|192.168.0.31|
|Office2|192.168.0.34|
|ns1.nethost.net  <br>(ISP)|198.28.2.254|

In this lab, your task is to troubleshoot and fix the issue using the following procedures:

- From the Office2 computer, use the ping and ipconfig commands to test connectivity and gather information.
    - Answer Questions 1 and 2.
- From the ITAdmin computer, use the ping and ipconfig commands to test connectivity and gather information.
    - Answer Questions 3 and 4.
- From the CorpServer computer, use the ping and ipconfig commands to test connectivity and gather information.
    - Answer Question 5 and determine which changes need to be made to correct the issue.
- Using the CorpDHCP server, accessed as a VM from CorpServer, implement the fix to the issue.
- Verify that the ITAdmin and Office2 computers can access the internet.
### Answer
![[TestOut LabSim425.pdf]]

---
## 4.2.6 Troubleshoot IP Configuration 2
### Prompt
You are a network technician for a small corporate network. The network is connected to the internet and uses DHCP for address assignments. The owner of the company in the Executive Office and a temporary employee in the IT Administrator office both report that their workstations can communicate with some computers on the network, but cannot access the internet. You need to diagnose and fix the problem.

While completing this lab, use the following IP addresses:

|   |   |
|---|---|
|Computer Name|IP Address|
|CorpServer|192.168.0.10|
|(Unknown)|198.28.2.254  <br>(the ISP)|
|ITAdmin|(Unknown)|
|Exec|(Unknown)|

In this lab, your task is to complete the following:

- To help troubleshoot the issue, use:
    - The ping, ipconfig, and tracert commands from the above computers.
    - The DHCP server console in the Windows Server 2019 operating system, which is running as a VM on the CorpServer computer.
- Fix the problem at the workstation, the DHCP server, or both as necessary.
- Use the troubleshooting tools to confirm the resolution of the problem.
### Answer
![[TestOut LabSim426.pdf]]

---
## 4.2.7 - Troubleshoot IP Configuration 3
### Prompt
You are a network technician for a small corporate network. The network is connected to the internet and uses DHCP for IP address assignments. The employee in Office 1 reports that their workstation can communicate with some computers on the network but not on the internet. You need to diagnose and fix the problem.

While completing this lab, use the following IP addresses:

|   |   |
|---|---|
|Computer Name|IP Address|
|CorpServer|192.168.0.10|
|Office1|192.168.0.30|
|Exec|192.168.0.33|
|ITAdmin|192.168.0.34|
|(Unknown)|198.28.2.254  <br>(the ISP)|

In this lab, your task is to:

- Use the following troubleshooting tools to diagnose the problem on the network:
    - The ping, ipconfig, or tracert command line utilities
    - The _Network & Internet settings_ on the Windows 10 operating system
- Fix the problem at the applicable workstation(s) as necessary.
- Use the troubleshooting tools to confirm that the problem is resolved.
### Answer
![[TestOut LabSim427.pdf]]

---
## 4.3.4 - Explore Network Communications
### Prompt
In this lab, you will discover important facts about network communications by using the **ping**, **ipconfig**, and **tracert** command utilities.

The following local network IP addresses are used in this lab:

|   |   |   |
|---|---|---|
|Location|Name|IP Address|
|Office 1|Office1|192.168.0.30|
|Support Office|Support|199.92.0.33|
|Router|Network Router|192.168.0.5|
|IT Administration|ITAdmin|192.168.0.33|
|ISP|External DNS Server|163.128.78.93|
|Router|Internet Router|198.28.56.1|

In this lab, your task is to:

1. Use the **ping** and **ipconfig** commands to troubleshoot network issues.
    1. Right-click **Start** and then select **Windows PowerShell (Admin)**.
    2. At the PowerShell prompt, type **ping 192.168.0.30** and press **Enter** to ping Office1.  
        You can successfully ping the IP address of Office1 from ITAdmin.
    3. Type **ping 199.92.0.33** and press **Enter** to ping Support.  
        You cannot ping Support from ITAdmin. Notice that the IP address for Support is on a different network (network 199.92.0.0 instead of network 192.168.0.0). Devices on the same local network must have IP addresses in the same network range. If you want to communicate with Support, you need to change the IP address assigned to Support.
    4. Type **ping 192.168.0.5** and press **Enter** to ping the router's internal interface.  
        You can successfully ping the router's internal interface from ITAdmin because ITAdmin and the router's address (192.168.0.5) are on the same network.
    5. Type **ipconfig** and then press **Enter** to view the IP settings.  
        Notice that there is no default gateway assigned.
    6. Type **ping 163.128.78.93** and press **Enter** to ping the external DNS Server.  
        ITAdmin and the ISP are on a different network (network 192.168.0.0 and 163.128.78.0, respectively). Because ITAdmin does not have a default gateway set, ITAdmin cannot communicate with devices on other networks.
2. Use the **tracert** command to see how network packets are forwarded.
    1. From the top left, select **Floor 1 Overview**.
    2. Under Executive Office, select **Exec**.
    3. Right-click **Start** and then select **Windows PowerShell (Admin)**.
    4. At the PowerShell prompt, type **tracert 198.28.56.1** and press **Enter**.  
        When you communicate with devices on other networks, the packets go to the default gateway first (the router between the two networks). The packets are sent to the router interface on the same network as the sending host and then to the next hop in the path. In this case, there are two IP addresses listed in the _tracert_ output, but only one router (hop) between Exec and the internet router. The last address in the _tracert_ output is the internet router.
    5. Enter **tracert 163.128.78.93** and press **Enter** to trace the path to one of the ISP's DNS servers.  
        When you trace the path between Exec and the ISP's DNS server, the path has additional hops. The first lines in the _tracert_ output are the routers (hops) between Exec and the DNS server. The last address in the _tracert_ output is the DNS server.
### Answer
![[TestOut LabSim434.pdf]]

---
## 4.4.4 Configure a DHCP Server
### Prompt
You are a network technician for a small corporate network. You want to use DHCP to provide TCP/IP address information to the workstations on the network. You already have a Windows Server 2022 server named CorpDHCP installed and running as a guest on CorpServer. You have installed the DHCP server role, and now you are ready to configure an IPv4 scope.

In this lab, your task is to:

- On the CorpDHCP server (running as a guest on CorpServer), create a DHCP IPv4 scope with the following parameters:
    - Scope name: **Subnet1**
    - Address range: **192.168.0.20** to **192.168.0.200**
    - Length: **24**
    - Subnet mask: **255.255.255.0**
    - Exclusions and delays: Do not set
    - Lease duration: Accept the default duration
    - Scope option for the router (default gateway): **192.168.0.5**
    - Parent domain: Accept the default
    - Scope option for DNS servers: **163.128.78.93**
    - WINS Servers: Do not set
- On CorpDHCP, activate the Subnet1 scope.
- On Gst-Lap in the Lobby, confirm the DHCP scope settings by configuring the local area connection to obtain its IP and DNS addresses automatically from the DHCP server.
### Answer
![[TestOut LabSim444.pdf]]

---
## 4.4.5 Configure DHCP Options
### Prompt
You have just configured a scope on the CorpDHCP server to service the 192.168.0.0/24 subnet. You need to configure additional TCP/IP parameters for all clients serviced by the CorpDHCP server.

In this lab, your task is to:

- Configure the following DHCP options for the CorpDHCP server (not on the Subnet1 scope):
    - 006 DNS Servers (in the following order):
        - **192.168.0.11**
        - **192.168.10.11**
    - 015 DNS Domain Name: **CorpNet.local**
- Configure Subnet1 scope options as follows:
    - 003 Router (default gateway) as **192.168.0.5**
### Answer
1. Access the CorpDCHP virtual server.
    1. From Hyper-V Manager, select **CORPSERVER**.
    2. Maximize the Hyper-V Manager window to view the available server.
    3. Right-click **CorpDHCP** and select **Connect**.
2. Configure the DHCP server options.
    1. From Server Manager, select **Tools** > **DHCP**.
    2. Maximize the DHCP window for better viewing.
    3. Expand **CorpDHCP.CorpNet.local** > **IPv4**.
    4. Right-click **Server Options** and select **Configure Options**.
    5. Under Available Options, select the **006 DNS Servers**.
    6. Enter **192.168.0.11** under _IP Address_.
    7. Select **Add** to add the IP address to the list.
    8. Under _IP Address_, enter **192.168.10.11** for the second server and then select **Add**.
    9. From the top pane, scroll down and select **015 DNS Domain Name**.
    10. In the _String value_ field, enter **CorpNet.local**.
    11. Select **OK** to save the options that you have defined.
3. Configure DHCP scope options.
    1. Expand **Scope [192.168.0.1] Subnet1**.
    2. Right-click **Scope Options** and select **Configure Options**.
    3. Under Available Options, select **003 Router**.
    4. Enter **192.168.0.5** under _IP address_.
    5. Select **Add** to add the IP address to the list.
    6. Select **OK** to save the options you defined

---
## 4.4.6 Create DHCP Exclusions
### Prompt
You have just configured a scope on the CorpDHCP server to service the 192.168.0.0/24 subnet. You defined a scope to distribute IP addresses between 192.168.0.1 and 192.168.0.254. However, some of the servers and other network devices on the network have been assigned static IP address in this range.

In this lab, your task is to:

- Prevent the DHCP server from assigning addresses.
    - Exclusion range: **192.168.0.1** to **192.168.0.29**
### Answer
Complete this lab as follows:

1. Access the CorpDHCP Hyper-V server.
    1. From Hyper-V Manager, select **CORPSERVER**.
    2. Resize the window to view all virtual machines.
    3. Double-click **CorpDHCP** to access the server.
2. Exclude the IP address range.
    1. From Server Manager's menu bar, select **Tools** > **DHCP**.
    2. Maximize the window for better viewing.
    3. Expand **CorpDHCP.CorpNet.local** > **IPv4** > **Scope [192.168.0.1] Subnet1**.
    4. Right-click the **Address Pool** node and select **New Exclusion Range**.
    5. Enter **192.168.0.1** in the _Start IP address_ field.
    6. Enter **192.168.0.29** in the _End IP address_ field.
    7. Select **Add**.
    8. Select **Close** to close the Add Exclusion Range dialog.

---
## 4.4.7 Create DHCP Client Reservations
### Prompt
You have several printers on Subnet1 that need static IP addresses assigned.

In this lab, your task is to:

- Use the CorpDHCP server.
- Configure the IPv4 scope.
- Use the following reservation information:

Use a _Support Type_ of **DHCP only** for each reservation.
    | Reservation  <br>Name | IP Address    | MAC Address       |
    | --------------------- | ------------- | ----------------- |
    | LaserJet4240-1        | 192.168.0.101 | aa:61:82:df:04:54 |
    | LaserJet4240-2        | 192.168.0.102 | ce:fd:48:90:06:23 |
    | KonicaColor           | 192.168.0.103 | c8:ba:99:cd:80:12 |
    | AcctPrinter           | 192.168.0.104 | f1:a9:3e:f7:7d:3b |
    | SalesPrinter          | 192.168.0.105 | df:a9:99:cd:80:61 |

### Answer
Complete this lab as follows:

1. Access the CorpDCHP virtual server.
    1. From Hyper-V Manager, select **CORPSERVER**.
    2. Maximize the Hyper-V Manager window to view the available server.
    3. Double-click **CorpDCHP** to connect to the server.
2. Configure the IP address.
    1. From Server Manager, select **Tools** > **DHCP**.
    2. Maximize the window for better viewing.
    3. From the left pane, expand _**CorpDHCP.CorpNet.local** > **IPv4** >_ **Scope [192.168.0.1] Subnet1**.
    4. Right-click **Reservations** and select **New Reservation**.
    5. In the _Reservation name_ field, enter a **reservation name**.
    6. In the _IP address_ field, enter the **IP address**.
    7. In the _MAC address_ field, enter the **MAC address**.
    8. Under Supported types, select **DHCP only** (as needed).
    9. Select **Add** to create the client reservation.
    10. Select **Yes** to the DHCP prompt.
    11. Repeat steps 2d - 2j for additional reservations.
    12. Select **Close**.

---
## 4.5.4 Configure a DHCP Relay Agent
### Prompt
You just installed DHCP service on the CorpDHCP server. You configured two scopes. The scope for Building A (Subnet1) is configured on the 192.168.0.0 network. The scope for Building B (Subnet2) is configured on the 192.168.10.0 network. After activating the scopes, you find that clients on Subnet1 receive IP addressing information from the DHCP server, but clients on Subnet2 have IP addresses in the 169.254.0.0/16 range. You realize that DHCP messages are not being forwarded through the router.

In this lab, your task is to:
- Use Routing and Remote Access to configure CorpServer2 as a DHCP Relay Agent by performing the following:
    - Add the DHCP Relay Agent routing protocol.
    - Add **NetTeam** as a DHCP Relay Agent interface.
    - Set the boot threshold to **0**.
    - Configure the DHCP Relay Agent properties to identify 192.168.0.14 as the DHCP server.
- Renew the TCP/IP information on Exec2 (the client machine in Building B).
- Verify that Exec2 has a network connection.
### Answer
![[Screenshot 2023-09-28 at 3.14.06 PM.png]]

---
## 4.5.5 Add a DHCP Server on Another Subnet
### Prompt
You have just authorized the CorpDHCP server to assign IP addresses to client workstations on the 192.168.10.0 subnet. You now need to create an IPv4 scope on the CorpDHCP server for an address range on this subnet.

In this lab, your task is to:
- Create an IPv4 scope on CorpDHCP using the following specifications:
    - IPv4 scope name: **Sales**
    - Address range: **192.168.10.21** to **192.168.10.199**
    - Default gateway: **192.168.10.5**
    - DNS servers: **198.28.56.108** and **163.128.78.93**
- Activate the new scope upon completion.
### Answer
![[Screenshot 2023-09-28 at 3.17.07 PM.png]]

---
## 4.6.4 Configure DHCP Failover 1
### Prompt
The CampusDHCP_1 server is currently the only DHCP server for clients on the 10.10.10.0/24 subnet. It has a scope that distributes addresses between 10.10.10.1 and 10.10.10.254 with an exclusion for static addresses for servers from 10.10.10.1 to 10.10.10.29.

To provide DHCP fault tolerance for this subnet, you plan to configure DHCP failover for the scope with the CampusDHCP_2 server (located on subnet 10.10.20.0/24 in Campus 2). Routers have been configured to pass DHCP requests between subnets.

In this lab, your task is to:
- Explore the DHCP configuration on CampusDHCP_1. Which scopes, exclusions, and options are configured?
- Explore the DHCP configuration on CampusDHCP_2. Which scopes, exclusions, and options are configured?
- On CampusDHCP_1, configure failover of the Campus1 scope with the CampusDHCP_2 server.
    - Failover mode: **Load balanced**
    - Load balance percentage for the local server: **75%**
    - Load balance percentage for the partner server: **25%**
    - Shared secret: **HelpMyDHCP123**
- Which scopes, exclusions, and options have been added to the CampusDHCP_2 server?

Use the navigation tabs to switch between servers and campus locations. CampusServer1 and CampusServer2 are Hyper-V host machines. The DHCP servers run as guest virtual machines on these servers.
### Answer
![[Screenshot 2023-09-28 at 3.53.44 PM.png]]

---
## 4.6.5 - Configure DHCP Failover 2

### Prompt
CampusDHCP_3 is currently the only DHCP server for clients on the 10.10.30.0/24 subnet. It has a scope that distributes addresses between 10.10.30.1 and 10.10.30.254 with an exclusion for static addresses for servers from 10.10.30.1 to 10.10.30.29. To provide DHCP fault tolerance for this subnet, you want to configure DHCP failover for the scope with the CampusDHCP_2 server (located on subnet 10.10.20.0/24 in Campus 2). Routers have been configured to pass DHCP requests between subnets.

In this lab, your task is to:
- On CampusDHCP_3, configure failover of the Campus3 scope with the CampusDHCP_2 server.
    - Failover mode: **Hot Standby**
    - Role of Partner Server: **Standby**
    - Addresses reserved for the standby server: **10%**
    - Shared Secret: **HelpMyDHCP456**
- Which scopes, exclusions, and options have been added to the CampusDHCP_2 server?

Use the top navigation menu to switch between servers and campus locations. CampusServer2 and CampusServer3 are Hyper-V host machines. The DHCP servers run as guest virtual machines on these servers.
### Answer
![[Screenshot 2023-09-28 at 3.55.39 PM.png]]

---
## 4.6.7 Configure a Scope for an Additional Subnet
### Prompt
You have authorized the CorpDHCP server to assign IP addresses to client workstations on the 192.168.10.0 subnet. Now you need to create an IPv4 scope on the CorpDHCP server for an address range on this subnet.

In this lab, your task is to:

- Access the Hyper-V server name CorpDHCP.
- Create an IPv4 scope on CorpDHCP using the following parameters:
    - IPv4 scope name: **Bldg-A Subnet**
    - Address range: **192.168.10.21** to **192.168.10.199**
    - Router (default gateway): **192.168.10.5**
    - DNS servers: **198.28.56.108** and **163.128.78.93**
- Activate the new scope upon completion.
### Answer
![[Screenshot 2023-09-28 at 4.11.40 PM.png]]

---
## 4.6.8 Configure a Split Scope
### Prompt
The CorpDHCP server is the only DHCP server for clients on the 192.168.0.0/24 subnet. This server has a scope that distributes addresses between 192.168.0.1 and 192.168.0.254 and an exclusion for static addresses for servers from 192.168.0.01 to 192.168.0.29. To provide DHCP fault tolerance for this subnet, you plan to split the scope with the CorpDHCP2 server (located on the 192.168.10.0/24 subnet in Building B). Routers have been configured to pass DHCP requests between subnets.

In this lab, your task is to:

- Explore the DHCP configuration on CorpDHCP and identify which scopes, exclusions, and options are currently configured.
- Add the CorpDHCP2 server to the DHCP console.
- Explore the DHCP configuration on CorpDHCP2 and identify which scopes, exclusions, and options are configured.
- On CorpDHCP, use the Split-Scope wizard to split the Subnet1 scope between CorpDHCP and CorpDHCP2.
    - Configure CorpDHCP to handle 85 percent of the IP addresses.
    - Configure CorpDHCP2 to handle 15 percent of the IP addresses.
    - Configure a 2 millisecond delay for the target server response.
    - Identify which exclusions have been added to the CorpDHCP server.
    - Identify which scopes, exclusions, and options have changed on the CorpDHCP2 server.
- Activate the backup scope for Subnet1 on CorpDHCP2.

This lab begins on CorpDHCP.
### Answer
![[Screenshot 2023-09-28 at 4.17.59 PM.png]]

---
## 4.7.5 Configure Alternate Addressing
### Prompt
You work as the IT administrator for a small corporate network. The receptionist in your office has a laptop. He took it home and configured a static connection to his home network. When he returned to the office, he could no longer connect to the office network, which uses a DHCP server for IP address configuration. You need to configure the laptop to work on both networks (home and office).

In this lab, your task is to:

- Verify the current state of the wireless network.
    - Answer the question.
- Configure the Wi-Fi adapter to obtain its:
    - IP address automatically
    - DNS server address automatically
- Configure the alternate TCP/IP information using the following information:
    - IP Address: **172.16.0.12**
    - Subnet Mask: **255.255.0.0**
    - Default Gateway: **172.16.255.254**
    - Preferred DNS Server: **198.60.22.2**
### Answer
![[Screenshot 2023-09-28 at 5.17.23 PM.png]]![[Screenshot 2023-09-28 at 5.17.47 PM.png]]

---
## 4.7.6 Troubleshoot DHCP 1
### Prompt
You are a network technician for a small corporate network. The network is connected to the internet and uses DHCP for address assignments. The employees in the Exec Office and Office 2 report that their workstations can communicate with some computers on the network, but not on the internet. The IP address for the ISP and internet is 198.28.2.254. The CorpDHCP server is a virtual server that runs on CorpServer.

In this lab, your task is to:

- Diagnose and fix the problem.

Use the following troubleshooting tools to accomplish the task:

- Command line utilities:
    - **ping**  
        (**ping** _**IP address** or **hostname**_)
    - **ipconfig**  
        (**ipconfig /all** or **ipconfig /renew**)
    - **tracert**  
        (**tracert** _**IP address** or **hostname**_)
- Network and Sharing Center.
- Network & Internet settings.
- The DHCP server console in the Windows Server operating system.
- The network diagram and schematic found in Exhibits.
### Answer
![[TestOut LabSim476.pdf]]

---
## 4.7.7 Troubleshoot DHCP 2
### Prompt
You are a network technician for a small corporate network. The network is connected to the internet and uses DHCP for address assignments. The owner of the company (in the Executive Office) and a temporary employee (in the IT Administrator office) both report that their workstations can communicate with some computers on the network, but not on the internet. The IP address for the ISP and the internet is 198.28.2.254.

In this lab, your task is to:

- Diagnose and fix the problem.

Use the following troubleshooting tools to accomplish the task:

- PowerShell/command line utilities:
    - **ping**  
        (**ping** **_IP address_** or **_hostname_**)
    - **ipconfig**  
        (**ipconfig /all** or **ipconfig /renew**)
    - **tracert**  
        (**tracert** _**IP address**_ or **_hostname_**)
- Network & Internet settings.
- The DHCP server console in the CorpDHCP server. The CorpDHCP server is a virtual server that runs on CorpServer.
- The network diagram and schematic found in Exhibits.
### Answer
![[TestOut LabSim477.pdf]]

---
## 4.8.8 Configure an IPv6 Address
### Prompt
You are the IT administrator for a small corporate network. The company has obtained the registered, globally unique IPv6 /48 network address 2620:14F0:45EA. You need to configure your server with this address so you can begin testing IPv6 in your internal network. This is your first network, so you will use a subnet address of 0001. Your network router is not configured for IPv6 yet, so you must manually configure the address for now. To simplify the configuration, use the server's IPv4 address to create the interface ID.

In this lab, your task is to:

- Locate the current IPv4 IP address for the external vEthernet network adapter.
- Answer Question 1.
- Configure the external vEthernet network adapter with the following IPv6 address:
    - Prefix: **2620:14F0:45EA:0001**
    - Interface ID: **_Use the current IPv4 address (in the correct format) for this adapter_**
    - Subnet prefix length: **64**
- Use **ipconfig** to verify the information.
### Answer
![[Screenshot 2023-09-29 at 11.48.28 AM.png]]

---
## 4.10.4 Configure NIC Teaming
### Prompt
You are the IT administrator for a small corporate network. You use CorpServer for your production server and need to have the most throughput possible. As a result, you need to configure NIC teaming.

In this lab, your task is to configure a NIC team on CorpServer as follows:

- Move the network cable from the onboard adapter in the CorpServer to the 4 port NIC in CorpServer.
- Connect network cables from the 4 port NIC on CorpServer to switch ports 19, 20, and 22.
- Configure the adapter ports as members of a NIC team using the following parameters:
    - Team name: **NetTeam**
    - Configure **Ethernet 3** through **Ethernet 6** as members of the team.
    - Teaming mode: **LACP**
    - Load balancing mode: **Address Hash**
    - Standby adapter: **None (all adapters Active)**
- Configure the Hyper-V Virtual Switch Manager to use the new NIC team for the External network, using the Microsoft Network Adapter Multiplexor Driver.
- Verify the status of the team and your network connection in Network and Sharing Center.
### Answer
![[TestOut LabSim4104.pdf]]

---
