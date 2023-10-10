---
aliases: [ "20231009170236",  ]
tags: SEC, SEC275
date_created: 2023-10-09 17:02
---
# Module 6 Labs
---
## 6.3.7 Create RODC Accounts
### Prompt
You are the IT administrator for a growing corporate network. Your network has a main office and two branch offices. Due to a recent expansion, you will be opening a new branch office. The new office will be part of the main site and will connect to the main office with a WAN link.

For security reasons, you plan to install a read-only domain controller in the new location.

In this lab, your task is to pre-create the RODC account in Active Directory as follows:

- Create a global security group named **Branch3-RODC Admins** in the Users container. Members of this group will be able to manage the read-only domain controller at the new location.
- Create the following RODC account in the Domain Controllers OU:
    - Name: **Branch3-RODC**
    - Specify your current credentials to complete the installation.
    - Add the account to the **Main-Site** site.
    - Make the domain controller a global catalog server and DNS server.
    - Identify the **Branch3-RODC Admins** group to manage the read-only domain controller.
### Answer

---
## 6.3.8 Edit the Password Replication Policy
### Prompt
You have just completed the installation of two read-only domain controllers, Branch3-RODC and Branch4-RODC. To allow logon when the WAN link to these sites is down, you want to configure the password replication policy to cache passwords for users who are likely to be at those locations. To increase security, you do not want to cache passwords for users who shouldn't be at that site.

You examine the users at each location and learn that:

- All members of the Sales team could use either the Branch3 or the Branch4 location.
- Only members of the Research-Dev team should use the Branch4 location.
- Mark Woods, a member of the Accounting department, will travel to both branches when performing audits.

In this lab, your task is to configure the password replication policy for Branch3-RODC and Branch4-RODC to cache only the necessary passwords using the following parameters:

- Edit the _Allowed RODC Password Replication Group_ group in the Users container. Add the following as members of the group:
    - **Sales** group
    - **Mark Woods** user account
    - To allow caching of computer account passwords, add:
        - All computer accounts in the Sales OU (**Sales1** through **Sales5**).
        - The **Acct2** computer account from the Accounting OU.
- Edit the properties for the Branch4-RODC account. Configure the password replication policy as follows:
    - Remove the group **Allowed RODC Password Replication Group**.
    - Add the group **Allowed RODC Password Replication Group** to the policy again, but with **Deny** permissions.
    - Add the **Research-Dev** group with **Allow** permissions.
    - Add the **Mark Woods** user account with **Allow** permissions.
    - Add the following computer accounts with Allow permissions to allow caching of computer account passwords:
        - From the Research OU: **ResM1**, **ResM2**, and **ResM3**
        - From the Accounting OU: **Acct2**
### Answer

---
## 6.4.6 Transfer RID and PDC Masters
### Prompt
You are the IT administrator for a small corporate network. When you installed the CorpDC domain controller, you created a new domain in a new forest. Since then, you've added additional domain controllers. You would like to move some of the operation master roles to CorpDC3 to provide role separation. You are currently logged on to the CorpServer2 computer, which is the Hyper-V host for CorpDC3.

In this lab, your task is to:

- Transfer the Relative ID (RID) master role to CorpDC3.
- Transfer the Primary Domain Controller (PDC) emulator role to CorpDC3.
### Answer

---
## 6.4.7 Transfer the Infrastructure Master
### Prompt
As your network has grown, you've added additional domains to the forest root domain. As a result, you would like to modify the operations master configuration on your network. You are currently logged on to the CorpServer2 computer, but you will complete these tasks using Hyper-V and the CorpDC4 server.

In this lab, your task is to:

- Transfer the Domain Naming Master role from CorpDC to CorpDC4.
    
    This means that CorpDC will only host the infrastructure master role.
    
- Remove the global catalog from CorpDC.
    
    This is required because you will create additional domains in the forest, and you want to follow Microsoft's recommendation not to place the infrastructure master on a global catalog server.
### Answer

---
## 6.4.8 Troubleshoot Operations Masters
### Prompt
You are the IT administrator for a small corporate network. These are the four domain controllers at the main location:

|   |   |
|---|---|
|Domain Controller|Current Role(s)|
|CorpDC|Infrastructure master|
|CorpDC2|None|
|CorpDC3|PDC emulator  <br>RID master|
|CorpDC4|Domain naming master|

Lately, you have had some problems creating new user objects in the domain. You suspect that one of your domain controllers has an intermittent problem connecting to the network. All domain controllers are currently working, but you want to prevent future problems of this nature.

In this lab, your task is to:

- Identify the operations master role that could cause the symptoms explained in the scenario.
- Transfer the correct operations master roles to the CorpDC2 domain controller.
### Answer

---
## 6.4.11 Configure Global Catalog Servers
### Prompt
You are the IT administrator for a small corporate network. You have four domain controllers in your main location, CorpDC, CorpDC2, CorpDC3, and CorpDC4. During installation, CorpDC2 and CorpDC3 were not made global catalog servers, but now you need some additional global catalog servers.

In this lab, your task is to designate CorpDC2 and CorpDC3 as global catalog servers.
### Answer

---
## 6.4.12 Enable Universal Group Membership Caching
### Prompt
You are the IT administrator for a small corporate network. You have a branch site with about 50 employees that is connected to the main site with a WAN link. A single domain controller named BranchDC2 is configured in the branch location. Because the WAN link is slow and unreliable, you have not configured BranchDC2 as a global catalog server. You find that when the WAN link goes down, users at the branch location cannot log on to the network. Even when the WAN link is up, users complain that the logon process is slow. You want to minimize Active Directory traffic across the WAN link, but you also want to let branch users log on to the network even when the WAN link is down.

In this lab, your task is to enable universal group membership caching in the branch office.
### Answer

---
## 6.5.3 Create a Forest Root Trust
### Prompt
You are the administrator for the CorpNet.local forest. Your network has the following domains: CorpNet.local, Branch1.CorpNet.local, and Branch2.CorpNet.local.

Your company works closely with another company. Their network has a single domain named PartnerCorp.xyz.

You need to let users in both forests access resources in both forests using the minimum number of trusts. Forest root trusts are transitive, meaning that the trust allows access to all child domains within the forest.

In this lab, your task is to create a forest root trust between the CorpNet.local and PartnerCorp.xyz forests.

- Create a forest root trust using the following settings:
    - Name of trust: **PartnerCorp.xyz**
    - Trust type: **Forest trust**
    - Direction of trust: **Two-way**
    - Sides of trust: **Domain only**
    - Outgoing trust authentication level: **Forest-wide authentication**
    - Trust password: **Trust@urF@r3st**
    - Do not confirm the trust.
- Create a forest root trust using the following settings:
    - Name of trust: **CorpNet.local**
    - Trust type: **Forest trust**
    - Direction of trust: **Two-way**
    - Sides of trust: **Domain only**
    - Outgoing trust authentication level: **Forest-wide authentication**
    - Trust password: **Trust@urF@r3st**
    - Confirm the outgoing and incoming trust.
### Answer

---
## 6.5.6 Design Trusts
### Prompt
You are the assistant IT administrator for a network with a single domain named PartnerCorp.xyz. Your company network has three domains, CorpNet.local, Branch1.CorpNet.local, and Branch2.CorpNet.local.

Management has decided that the full cross-forest trust you created is too much of a security risk. However, the board of directors for PartnerNet still needs access to financial resources that are in the Branch1.CorpNet.local domain.

Only the members of the Directors group should be allowed to access the domain. Other users at PartnerNet should not be able to access Branch1.CorpNet.local, and users in CorpNet should not be able to access the PartnerCorp.xyz domain.

In this lab, your task is to create trust relationship(s) with the CorpNet network to meet the requirements specified in the scenario above.

- You are currently working at CampusServer1, which is a Hyper-V host. Domain controllers for the PartnerCorp.xyz domain run as guests on this server.
- Create both sides of the trust.
- As necessary, use the following usernames and passwords to connect to the destination domain:
    |Domain|Username|Password|
    |CorpNet.local|Administrator|1Drowss@p!@#|
    |Branch1.CorpNet.local|Administrator|2ManyP@ssw0rds|
    |Branch2.CorpNet.local|Administrator|goingFISHing@5|
    
- Any additional configuration required in the CorpNet.local forest beyond creating the trust relationship will be performed by administrators in their respective domains.
### Answer

---
## 6.5.7 Create a Shortcut Trust
### Prompt
Your company has the following Active Directory domains:

- CorpNet.local
- Branch1.CorpNet.local
- Branch2.CorpNet.local

Users in the Branch1.CorpNet.local and Branch2.CorpNet.local domains frequently share resources. Users have commented that authentication is slow. You want to speed up authentication between these two domains. You are currently on the BranchDC1 server.

In this lab, your task is to:

- Create a new shortcut trust between the Branch1.CorpNet.local and Branch2.CorpNet.local domains. This can be accomplished from either domain. When creating the trust, use the following parameters:
    |Domain|Password|
    |Branch1.CorpNet.local|2ManyP@ssw0rds|
    |Branch2.CorpNet.local|goingFISHing@5|
    

- Create a shortcut trust using the following settings:
    - Username: **Administrator**
    - Trust type: **Forest trust**
    - Direction of trust: **Two-way**
    - Sides of trust: **Both this domain and the specified domain**
    - Local domain trust authentication level: **Domain-wide authentication**
    - Specified domain trust authentication level: **Domain-wide authentication**
    - Confirm the outgoing and incoming trust.
### Answer

---
## 6.6.4 Configure Sites
### Prompt
You are assisting the administrator of the CorpNet.local domain. Your company has three office locations named Main, Branch1, and Branch2. All of the locations are connected to each other with wide area network (WAN) links. Domain controllers are installed for each location, but each domain controller is still located in the _Default-First-Site-Name_ site.

In this lab, your tasks is to:

- Rename the _Default-First-Site-Name_ site to **Main-Site**.
- Create new sites for the branch offices using **DEFAULTSITELINK** as the site link object.
- Move the branch servers into their respective sites.
- Create a subnet for all the sites and choose the corresponding site object.

Configure sites and subnets using the following table:

|              |                                               |                                     |
| ------------ | --------------------------------------------- | ----------------------------------- |
| Site Name    | Server                                        | Subnet                              |
| Main-Site    | CorpDC  <br>CorpDC2  <br>CorpDC3  <br>CorpDC4 | 192.168.0.0/24  <br>192.168.10.0/24 |
| Branch1-Site | BranchDC1                                     | 192.168.20.0/24                     |
| Branch2-Site | BranchDC2                                     | 192.168.30.0/24                     |
### Answer

---
## 6.6.5 Manage Sites and Subnets
### Prompt
You are assisting the administrator for the PartnerNet.xyz domain. The company has three office locations, which are named Campus1, Campus2, and Campus3. All locations are connected to each other using wide area network (WAN) links (see exhibits). Domain controllers for each location have been installed, but each domain controller is still located in the Default-First-Site-Name site.

In this lab, your task is to complete the following:

- Delete the Default-First-Site-Name site or rename it as one of the three sites in the table.
- Create and configure three sites and subnets as follows:
    
    |Site Name|Subnet|Servers|
    |Campus1-Main-Site|10.10.10.0/24|CampusDC1  <br>CampusDC4|
    |Campus2-Site|10.10.20.0/24|CampusDC2|
    |Campus3-Site|10.10.30.0/24|CampusDC3|
    
- Move the domain controllers into their applicable corresponding sites.
- Delete the DEFAULTIPSITELINK site link or rename and configure it as one of your three site links in the table.
- Create and configure three site links as follows:
    
    | Site Link Name  | Sites in the Site Link              |
    | --------------- | ----------------------------------- |
    | Campus1-Campus2 | Campus1-Main-Site  <br>Campus2-Site |
    | Campus1-Campus3 | Campus1-Main-Site  <br>Campus3-Site |
    | Campus2-Campus3 | Campus2-Site  <br>Campus3-Site      |
### Answer

---
## 6.7.5 Configure Intrasite Replication
### Prompt
You are the IT administrator for a growing corporate network. You want to make sure new users can log on to the network using any of the site's domain controllers as soon as possible after a user account is created.

In this lab, your task is to:

- Connect to the CorpDC virtual server.
- Configure the NTDS Site Settings for the Main-Site with a replication schedule that replicates as often as possible per hour.
### Answer

---
## 6.7.6 Configure Intersite Replication
### Prompt
You are assisting the administrator of the PartnerCorp.xyz domain. The company has three main campus locations, Campus1, Campus2, and Campus3. All locations are connected to each other using wide area network (WAN) links. You have configured a site for each physical site location in Active Directory Sites and Services. You have also configured a site link for each WAN link.

You need to customize Active Directory replication to accomplish the following goals:

- Replication between the Campus2 and Campus3 sites should use the 20 Mbps line only if one of the links to the Campus1 site is unavailable. In other words, Active Directory replication should use the site links from Campus3 to Campus1 and from Campus1 to Campus2.
- To reduce WAN traffic on the link, replication between Campus1 and Campus2 should only occur during the hours of 8:00 p.m. and 6:00 a.m. Monday through Friday. Replication is allowed during all hours on the weekend.
- Replication from Campus1 to Campus2, and from Campus1 to Campus3 should occur once per hour during the hours that replication is allowed.
- Replication between sites originating from the Campus1 site should only use CampusDC1. CampusDC4 should not be used for inter-site replication.

In this lab, your task is to customize replication as follows:

- For the Campus1-Campus2 site link, use the following settings:
    - Cost: **110**
    - Replication frequency: **60 minutes**
    - Replication schedule:
        - Sunday: **allow all day**
        - Monday through Friday: **allow 8:00 p.m. to 6:00 a.m.**
        - Saturday: **allow all day**
- For the Campus2-Campus3 site link, use the following settings:
    - Cost: **300**
    - Replication frequency: **175 minutes**
    - Replication schedule:
        - Sunday through Friday: **allow all day**
        - Saturday: **allow 12:00 a.m. to  5:00 p.m.**
- For the Campus1-Campus3, site link use the following settings:
    - Cost: **110**
    - Replication frequency: **60 minutes**
    - Replication schedule:
        - Sunday through Friday: **allow all day**
        - Saturday: **allow 12:00 a.m. to  5:00 p.m.**
- Designate CampusDC1 as the preferred bridgehead server for IP.
### Answer

---
