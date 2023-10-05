

aliases: [ "20230918102112",  ]
tags: SEC, SEC203, TestOutSec
date_created: 2023-09-18 10:21

# Module 4 Labs
---
## 4.2.5 Configure Automatic Updates
### Prompt
You need to customize how Windows Update checks for and installs updates on the ITAdmin desktop system.

In this lab, your task is to:

- Configure Windows Update to:
    - Install updates for other Microsoft products when Windows is updated.
    - Allow the installation of feature updates to be deferred 60 days.
    - Allow quality updates to be deferred 30 days.
- Configure Windows to automatically download manufacturers' apps and custom icons for devices.
### Answer
![[Screenshot 2023-09-18 at 10.24.22 AM.png]]

---
## 4.2.7 Configure Microsoft Defender Firewall
### Prompt
You have a new laptop that is running Windows 10. You notice a security message that indicates that Windows Firewall has been disabled. The laptop is currently connected to your organization's network, and the Domain network profile settings are in effect. You plan to travel this week, and you will connect the laptop to various airport Wi-Fi hotspots. You need to enable Windows Firewall for any public network.

In this lab, your task is to configure Windows Firewall as follows:

- Turn on Windows Firewall for the Public network profile only.
- In addition to the programs and ports currently allowed, allow the following service and programs through the firewall for the Public network profile only:
    - A service named **Key Management Service**
    - An application named **Arch98**
    - An application named **Apconf**

### Answer
![[Screenshot 2023-09-18 at 10.32.15 AM.png]]

---
## 4.3.5 - Configure NTFS Permissions
### Prompt
There are two groups of users who access the CorpFiles server, Marketing and Research.
Each group has a corresponding folder:
- D:\Marketing Data
- D:\Research Data

In this lab, your task is to:
1. Disable permissions inheritance for **D:\Marketing Data** and **D:\Research Data** and convert the existing permissions to explicit permissions.
2. For each of the above folders, remove the **Users** group from the access control list (ACL).
3. Add the **Marketing** group to the Marketing Data folder ACL.
4. Add the **Research** group to the Research Data folder ACL.
5. Assign the groups **Full Control** to their respective folders.
6. Do not change any other permissions assigned to other users or groups.

### Answer
![[Screenshot 2023-09-18 at 11.13.52 AM.png]]

---
## 4.3.6 Disable Inheritance
### Prompt
Confidential personnel data is stored on the CorpFiles file server in a shared directory named Personnel. You need to configure NTFS permissions for this folder so that only managers are authorized to access it.

In this lab, your task is to perform the following:
- Grant the Managers group the **Full Control** permission to the **D:\Personnel** folder.
- Remove all inherited permissions that are flowing to the **D:\Personnel** folder.

If a permission appears grayed out, it is an inherited permission. To modify it, you need to disable inheritance and create explicit permissions.

### Answer
![[Screenshot 2023-09-18 at 11.17.54 AM.png]]
