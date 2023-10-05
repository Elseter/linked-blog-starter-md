


aliases: [ "20230925151234",  ]
tags: SEC, SEC203, TestOutSec
date_created: 2023-09-25 15:12

# Module 5 Labs
---
## 5.1.7  - Configure a Security Appliance
### Prompt
You are an IT security administrator for a small corporate network. To increase security for the corporate network, you have installed the pfSense network security appliance in your network. Now you need to configure the device.

In this lab, your task is to configure pfSense as follows:

- Sign in to pfSense using the following case-sensitive information:
    - URL: **198.28.56.18**
    - Username: **admin**
    - Password: **pfsense**
- Configure the DNS servers as follows:
    - Primary DNS server: **163.128.78.93** - Hostname: **DNS1**
    - Secondary DNS server: **163.128.80.93** - Hostname: **DNS2**
- Configure the WAN IPv4 information as follows:
    - Enable the interface.
    - Use a static IPv4 address of **65.86.24.136/8**
    - Add a new gateway using the following information:
        - Type: **Default gateway**
        - Name: **WANGateway**
        - IP address: **65.86.1.1**
### Answer
![[Screenshot 2023-09-25 at 3.16.54 PM.png]]
![[Screenshot 2023-09-25 at 3.17.05 PM.png]]

---
## 5.1.8 - Configure Network Security Appliance Access
### Prompt
You work as the IT security administrator for a small corporate network. You need to secure access to your pfSense appliance, which is still configured with the default user settings.
In this lab, your task is to:
- Change the password for the default pfSense account from pfsense to **P@ssw0rd (use a zero).**
- Create a new administrative user with the following parameters:
    - Username: **zolsen**
    - Password: **St@yout!**
    - Full Name: **Zoey Olsen**
    - Group Membership: **admins**
- Set a session timeout of **15** minutes for pfSense.
- Disable the webConfigurator anti-lockout rule for HTTP.

Access the pfSense management console through Google Chrome using: http://198.28.56.18
- Default username: **admin**
- Password: **pfsense**
### Answer
![[Screenshot 2023-09-25 at 3.29.43 PM.png]]
![[Screenshot 2023-09-25 at 3.30.01 PM.png]]

---
## 5.1.10 - Configure QoS
### Prompt
You are the IT administrator for a small corporate network. Several employees have complained of slow internet bandwidth. You have discovered that the user stations on the guest Wi-Fi network are consuming much of your company's bandwidth. You have decided to use pfSense's Traffic Shaper wizard to create the various rules needed to better control the bandwidth usage and to fine-tune the priority for the type of traffic used on your guest Wi-Fi network.

Your network has one LAN and one WAN.

In this lab, your task is to:

- Access the pfSense management console:
    - Username: **admin**
    - Password: **P@ssw0rd** (zero)
- Create a firewall alias using the following specifications:
    - Name: **HighBW**
    - Description: **High bandwidth users**
    - Assign the IP addresses of the high-bandwidth users to the alias:
        - Vera's IP address: **172.14.1.25**
        - Paul's IP address: **172.14.1.100**
- The Shaper must be configured for the GuestWi-Fi interface using:
    - An upload bandwidth of **5** Mbits
    - A download bandwidth of **45** Mbits
- Allow your voice over IP traffic to have priority with:
    - An upload bandwidth of **15** Mbits
    - A download bandwidth of **20** Mbits
- To limit the user stations most likely to hog bandwidth, use the alias created earlier to penalize the offending stations to 2% of the bandwidth.
- Give a higher priority to the following services and protocols:
    - MSRDP
    - VNC
    - PPTP
    - IPSEC
- Change the port number used on the floating rule created for MSRDP as follows:
    - Interface: **GuestWi-Fi**
    - Destination Port Range: **3391**
- Answer the question.
### Answer
![[Screenshot 2023-09-25 203852.png]]
![[Screenshot 2023-09-25 203921.png]]

---
## 5.2.3 - Configure a DMZ
### Prompt
You are the IT administrator for a small corporate network. You want to make a web server that runs services accessible from the internet. To help protect your company, you want to place this server and other devices in a demilitarized zone (DMZ). This DMZ and server need to be protected by the pfSense Security Gateway Appliance (pfSense). Since a few of the other devices in the DMZ require an IP address, you have also decided to enable DHCP on the DMZ network.

In this lab, your task is to perform the following:
- Access the pfSense management console:
    - Username: **admin**
    - Password: **P@ssw0rd** (zero)
- Add a new pfSense interface that can be used for the DMZ.
    - Name the interface **DMZ**.
    - Use a static IPv4 address of **172.16.1.1/16**
- Add a firewall rule for the DMZ interface that allows all traffic from the DMZ.
    - Use a description of **Allow DMZ to any rule**
- Configure and enable the DHCP server for the DMZ interface.
    - Use a range of **172.16.1.100** to **172.16.1.200**
### Answer
![[Screenshot 2023-09-25 210155.png]]

---
## 5.3.5 Configure a Perimeter Firewall
### Prompt
You work as the IT security administrator for a small corporate network. You recently placed a web server in the demilitarized zone (DMZ). You need to configure the perimeter firewall on the network security appliance (pfSense) to allow access from the WAN to the Web server in the DMZ using both HTTP and HTTPs. You also want to allow all traffic from the LAN network to the DMZ network.

In this lab, your task is to:

- Access the pfSense management console:
    - Username: **admin**
    - Password: **P@ssw0rd** (zero)
- Create and configure a firewall rule to pass HTTP traffic from the WAN to the Web server in the DMZ.
- Create and configure a firewall rule to pass HTTPS traffic from the WAN to the Web server in the DMZ.
    - Use the following table when creating the HTTP and HTTPS firewall rules:
| Parameter                | Setting                                                              |
| ------------------------ | -------------------------------------------------------------------- |
| Source                             | WAN network                                                          |
| Destination port/service | HTTP (80), HTTPS (443)                                               |
| Destination                     | A single host                                                        |
| IP address for host          | 172.16.1.5                                                           |
| Descriptions                    | For HTTP: HTTP from WAN to DMZ  For HTTPS: HTTPS from WAN to DMZ |
- Create and configure a firewall rule to pass all traffic from the LAN network to the DMZ network. Use the description _LAN to DMZ Any_.
### Answer
![[Screenshot 2023-09-25 212831.png]]

---
## 5.4.3 Configure NAT
### Prompt
You are the IT administrator for a small corporate network. One of your assignments is to manage several computers in the demilitarized zone (DMZ or screened subnet). However, your computer resides on the LAN network. To be able to manage these machines remotely, you have decided to configure your pfSense device to allow several remote control protocols to pass through the pfSense device using NAT port forwarding.

In this lab, your task is to create NAT forwarding rules:
- Access the pfSense management console:
    - Username: **admin**
    - Password: **P@ssw0rd** (zero)
- Allow the RDP/TCP Protocols from the LAN network to the PC1 computer located in the DMZ using the following:
    - IP address for PC1: **172.16.1.100**
    - Description: **RDP from LAN to PC1**
- Allow the SSH Protocol through the from the LAN network to the Kali Linux server located in the DMZ using the following:
    - IP address for the Linux Kali server: **172.16.1.6**
    - Description: **SSH from LAN to Kali**
- Allow the RDP/TCP Protocols from the LAN network to the web server located in the DMZ using the following:
    - Destination and redirect port: **Port 5151**
    - IP address for the web server: **172.16.1.5**
    - Description: **RDP from LAN to web server using custom port**
### Answer
![[Screenshot 2023-09-26 092704.png]]

---
## 5.5.4 Configure a Remote Access VPN
### Prompt
You work as the IT security administrator for a small corporate network. Occasionally, you and your co-administrators need to access internal resources when you are away from the office. You would like to set up a Remote Access VPN using pfSense to allow secure access.

In this lab, your task is to use the pfSense wizard to create and configure an OpenVPN Remote Access server using the following guidelines:

- Sign in to pfSense using:
    - Username: admin
    - Password: P@ssw0rd (zero)
- Create a new certificate authority certificate using the following settings:
    - Name: **CorpNet-CA**
    - Country Code: **GB**
    - State: **Cambridgeshire**
    - City: **Woodwalton**
    - Organization: **CorpNet**
- Create a new server certificate using the following settings:
    - Name: **CorpNet**
    - Country Code: **GB**
    - State: **Cambridgeshire**
    - City: **Woodwalton**
- Configure the VPN server using the following settings:
    - Interface: **WAN**
    - Protocol: **UDP on IPv4 only**
    - Description: **CorpNet-VPN**
    - Tunnel network IP: **198.28.20.0/24**
    - Local network IP: **198.28.56.18/24**
    - Concurrent Connections: **4**
    - DNS Server 1: **198.28.56.1**
- Configure the following:
    - A firewall rule
    - An OpenVPN rule
- Set the OpenVPN server just created to **Remote Access (User Auth)**.
- Create and configure the following standard remote VPN users:
    | Username  | Password   | Full Name      |
    | --------- | ---------- | -------------- |
    | blindley  | L3tM31nNow | Brian Lindley  |
    | jphillips | L3tM31nToo | Jacob Phillips |
### Answer
![[Screenshot 2023-09-26 095144.png]]

---
## 5.5.5 Configure a VPN Connection iPad
### Prompt
You work as the IT security administrator for a small corporate network. You recently set up the Remote Access VPN feature on your network security appliance to provide you and your fellow administrators with secure access to your network. You are currently at home and would like to connect your iPad to the VPN. Your iPad is connected to your home wireless network.

In this lab, your task is to:
- Add an IPSec VPN connection using the following values:
    This can be added by selecting **Settings** > **General** > **VPN**.
    |Parameter|Value|
    |Description|**CorpNetVPN**|
    |Server|**198.28.56.34**|
    |Account|**mbrown**|
    |Secret|**asdf1234$**|
    
- Turn on the VPN.
- Verify that a connection is established. The password for mbrown is **L3tM31nN0w** (0 = zero).
### Answer
![[Screenshot 2023-09-26 100229.png]]

---
## 5.6.3 Configure URL Blocking
### Prompt
- You are the security analyst for a small corporate network. After monitoring your network, you have discovered that several employees are wasting time visiting non-productive and potentially malicious websites. As such, you have added pfBlockerNG to your pfSense device. You now need to configure this feature and add the required firewall rules that allow/block specific URLs and prevent all DNS traffic from leaving your LAN network.
    
    In this lab, your task is to:
    
    - Sign in to pfSense using:
        - Username: admin
        - Password: P@ssw0rd (zero)
    - Create a firewall rule that blocks all DNS traffic leaving the LAN network.
    - Create a firewall rule that allows all DNS traffic going to the LAN network.
    
    Use the following table for the two rules:
    |Parameter|Setting|
    |Protocol|UDP (53)|
    |Descriptions|For the block rule: **Block DNS from LAN**  <br>For the allow rule: **Allow all DNS to LAN**|
    
- Arrange the firewall rules in the order that allows them to function properly.
- Enable and configure pfBlockerNG using the information in the following table:
    | Parameter                        | Setting                                                                    |
    | -------------------------------- | -------------------------------------------------------------------------- |
    | DNSBL Virtual IP                 | **192.168.0.0**                                                            |
    | Top-Level Domain (TLD) Blacklist | - **financereports.co**<br>- **totalpad.com**<br>- **salesscript.info**    |
    | Top-Level Domain (TLD) Whitelist | - **.www.google.com**<br>- **.play.google.com**<br>- **.drive.google.com** |
### Answer
![[Screenshot 2023-09-26 102601.png]]![[Screenshot 2023-09-26 102624.png]]

---

## 5.9.6 Secure a Switch
### Prompt
You are the IT security administrator for a small corporate network. You need to secure access to your switch, which is still configured with the default settings.

Access the switch management console through Chrome on **http://192.168.0.2** with the username **cisco** and password **cisco**.

In this lab, your task is to:
- Create a new user account with the following settings:
    - Username: **ITSwitchAdmin**
    - Password: **Admin$only1844**
    - User Level: **Read/Write Management Access (15)**
- Edit the default user account as follows:
    - Username: **cisco**
    - Password: **CLI$only1958**
    - User Level: **Read-Only CLI Access (1)**
- Save the changes to the switch's startup configuration file.
### Answer
![[Screenshot 2023-09-26 at 12.54.47 PM.png]]
