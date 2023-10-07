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
![[Screenshot 2023-10-06 at 2.25.29 PM.png]]

---
## 5.1.6 - Create Host Records
### Prompt
You work as the IT administrator for a small corporate network. You have two servers and a DNS server that use static IP addresses on the 192.168.0.0/24 subnet. You plan to install three more servers soon, so you need to create DNS records for these servers on the CorpDC server.

In this lab, your task is to
- Create an IPv4 Active Directory-integrated primary reverse lookup zone for subnet 192.168.0.0/24. Be sure to accept the default replication and dynamic update settings.
- Create A records and PTR records under CorpNet.local for the following hosts:
    |Host Name|IP Address|
    |CorpServer|192.168.0.10|
    |CorpFiles16|192.168.0.12|
    |CorpFiles12|192.168.0.13|
    |CorpDHCP|192.168.0.14|
    |CorpWeb|192.168.0.15|
    

If you create the A records before creating the reverse lookup zone, the PTR records will not be created automatically.
### Answer
![[Screenshot 2023-10-06 at 2.30.55 PM.png]]

---
## 5.1.7 Create CNAME Records
### Prompt
The sales department wants to create an intranet for all sales employees. Internet Information Services (IIS) is installed on CorpWeb and will be used to host the intranet site. Employees need the ability to access the web server using any of the following URLs:

- http://sales.private
- http://intranet.sales.private
- http://www.sales.private

You have already created the sales.private forward lookup zone on the CorpDC server.

In this lab, your task is to:

- Allow connections to the web server by creating the following ALIAS (CNAME) records in the zone using the following information:

    |**ALIAS Name**|**Target Host (FQDN)**|
    |_(leave blank)_|CorpWeb.CorpNet.local|
    |intranet|CorpWeb.CorpNet.local|
    |www|CorpWeb.CorpNet.local|

When creating ALIAS records, use CorpWeb.CorpNet.local as the fully qualified domain name.
### Answer
![[Screenshot 2023-10-06 at 3.44.51 PM.png]]

---
## 5.1.8 - Troubleshoot DNS Records
### Prompt
Listen to simulation instructions

You are the administrator for the CorpNet.local domain. The CorpDC and CorpDC3 servers are the DNS servers for the domain. You are responsible for CorpDC, which resides in Building A. Some users report that they are unable to contact the CorpWeb server.

In this lab, your task is to:

- Test the connectivity to CorpWeb using the **ping** command.
    - Ping **CorpWeb.CorpNet.local**
    - Ping **192.168.0.15** (the IP address for CorpWeb).
    - Answer Question 1.
- Create any DNS records needed to fix the problem using the following information:
    - Host name: **CorpWeb**
    - IP address: **192.168.0.15**
- Test the connectivity to CorpWeb using the **ping** command.
    - Ping **CorpWeb.CorpNet.local**
    - Ping **192.168.0.15** (the IP address for CorpWeb).
    - Answer Question 2.
### Answer
![[Screenshot 2023-10-06 at 3.52.43 PM.png]]

---
## 5.2.5 - Configure Forwarders
### Prompt
You work as the IT administrator for a small corporate network. The server CorpDC is your domain controller and DNS server. This server hosts the CorpNet.xyz zone. For name resolution requests in other zones, you want CorpDC to forward requests to name servers at the ISP.

In this lab, your task is to configure the DNS service on CorpDC using the following settings:

- Forward name resolution requests outside of the CorpNet.xyz domain to the following ISP DNS servers:
    - 163.128.80.93
    - 163.128.78.93
- Use root hints for requests if the ISP DNS servers are unavailable.
### Answer
![[Screenshot 2023-10-06 at 7.46.43 PM.png]]

---
## 5.2.6 - Create a Root Zone
### Prompt
You work as the IT administrator for a small business and are responsible for the corporate network. A partner company has asked you to help configure their DNS server.

CAMPUSDC1 is a Windows Server 2022 server that holds the primary copy of the PartnerNet.xyz domain. The server is in a screened subnet, or demilitarized zone (DMZ), and provides name resolution for the domain for internet hosts.

The partner company wants to prevent CAMPUSDC1 from performing name resolution requests for domains other than the PartnerNet.xyz domain. In other words, they do not want internet hosts to be able to obtain name resolution from CAMPUSDC1 for domains outside the company.

In this lab, your task is to:

- Verify that Root Hints are being provided.
    - Answer Question 1.
- Create a new forwarding lookup zone on CAMPUSDC1.
    - Zone named: **.** _(a dot to represent the root zone.)_
    - Do not allow dynamic updates.
- Verify that root hints are no longer configured on the server.
    - Answer Question 2.
### Answer
![[Screenshot 2023-10-06 at 7.49.52 PM.png]]

---
## 5.3.7 - Create an Active Directory-Integrated Zone
### Prompt
You work as the IT administrator for a small business and are responsible for the corporate network. The marketing department wants to create an intranet site that is only accessible from the private network. You have selected mrktg.private as the domain name that will hold all records for the zone. You want all client computers in the domain to update their records automatically using DNS. Because security is important, you need to make sure that only the computer that created the DNS record can update it.

You also need to create an Active Directory–integrated zone to store the zone data in Active Directory. Using an Active Directory–integrated zone lets you use a multi-master approach to storing zone data. These types of zones also support secure dynamic DNS updates. You can only create Active Directory–integrated zones on DNS servers that are domain controllers.

In this lab, your task is to:

- Create a forward lookup zone on the CorpDC DNS server using the following guidelines:
    - Zone type: **Primary** (stored in Active Directory)
    - Replicate data: **To all DNS servers in the CorpNet.local forest**
    - Zone name: **mrktg.private**
    - Dynamic update type: **Allow only secure dynamic updates**
### Answer
![[Screenshot 2023-10-07 at 4.45.46 PM.png]]

---
## 5.3.8 - Convert a Zone to Active Directory-integrated
### Prompt
The CorpDC server currently stores the sales.private standard primary DNS zone. You need to configure the sales.private zone to store all the data in Active Directory.

In this lab, your task is to complete the following:

- Convert the **sales.private** zone to an Active Directory-integrated zone.
- Change the replication scope to store data on all DNS servers in the domain.

The zone must exist on a domain controller before it can be converted to an Active Directory-integrated zone.
### Answer
![[Screenshot 2023-10-07 at 4.48.16 PM.png]]