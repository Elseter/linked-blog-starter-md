---
aliases:
  - "20231003100353"
tags:
  - SEC
  - SEC275
  - TestOutServer
date_created: 2023-10-03 10:03
Index: "[[SEC.275 Index]]"
---
# Module 5 Labs
---
## 5.1.4 - Configure DNS Addresses
### Prompt 
You are helping a friend in college with his network connection. The dormitory where he lives has installed a 1000BaseT Ethernet network. This network uses a DHCP server to assign the IP addressing. You would like to configure your friend's computer (named Dorm-PC) to use a different set of DNS server addresses than the ones being delivered by the DHCP server.

In this lab, your task is to:

- Configure the IPv4 settings for the Ethernet network card to use the following DNS server addresses:
    - Preferred DNS server: **208.67.222.222**
    - First alternate DNS server: **208.67.222.220**
    - Second alternate DNS server: **208.67.220.123**
    - Validate the static DNS server information.
### Answer
![[Screenshot 2023-10-03 at 10.07.05 AM.png]]

---
## 5.1.5 - Create Standard DNS Zones
### Prompt
The accounting department is testing a new payroll system server. To facilitate their tests, they would like to add the payroll server to DNS to support name resolution. You need to create a new zone to support their request and accelerate lookups. You also need to place a copy of this zone on the DNS server in Building B.

In this lab, your task is to:

- Create a primary forward lookup zone on CorpDC using the following parameters:
    - Deselect **Store the zone in Active Directory**.
    - Use **acct.CorpNet.local** as the zone name.
    - Use the default name for the zone file.
    - Do not allow dynamic updates.
    - Allow zone transfers to any server.
- Create a secondary forward lookup zone called **acct.CorpNet.local** on CorpDC3.
    - Specify **192.168.0.11** or **CorpDC.CorpNet.Local** as the master DNS server for the zone.
### Answer
