
---
aliases: [ "20230222150545",  ]
tags: SEC.101, SEC, PCPro
date_created: 2023-02-22 15:05
---
[[SEC.101 Index]]
# TestOut PC Pro - 6.2
---
## 6.2.8 Installation Facts
- This lesson covers the following topics
	- Installation methods
	- Installation process

### Installation methods
#### External Drive
When installing from an external drive such as a USB drive, solid-state external drives, or hot swappable drives, keep the following items in mind:

-   The drive must have sufficient storage space available.
-   The drive can store both the Windows source files, as well as additional software and drivers.
-   Change the boot order in the BIOS/UEFI configuration to boot from the external drive first.
-   Connect the drive before restarting the computer.

#### Optical Media
When performing a clean install from an optical drive (DVD), complete the following tasks:

-   Change the boot order to boot from the optical drive first.
-   Start the installation by booting the computer from the installation disc.
-   Load the drivers for the RAID array controller if using a hardware RAID array as the destination disk.

#### ISO
You can download the Windows installation media in an .ISO format. An ISO file (sometimes referred to as an ISO image) is an archive file that contains an identical copy (or image) of data found on an optical disc, such as a DVD.  
  
You can burn ISO files to a DVD or put them on a USB drive. Windows can mount ISO files directly and run the installation software from the location where it was downloaded.  
  
To install from the ISO file on an existing Windows system:

-   Right-click the ISO file.
-   Select **Mount**.
-   From the mount point, run the setup.exe file.

#### Image Deployment
Another installation option is to use disk imaging. With disk imaging, you install a base Windows system on one computer. You then use the disk duplication process to copy that system's hard drive to the hard drives of other computers. Imaging is usually faster than the traditional Windows installation process and is suitable for situations where you need to run simultaneous installations. Keep in mind:

-   Because of driver support issues, imaging works best when the hardware on the destination system is the same as the hardware on the source system.
-   Image deployment works best if a volume license is used on the reference system.
-   If a standard license is used, you will need to relicense each imaged system separately.

#### Remote network installation
In an enterprise environment, you can use a network install. To do this, you configure the system to boot from its network interface. This is done using the pre-boot execution environment (PXE). During a PXE boot:

-   The system connects to a Windows Remote Installation server over the network.
-   It loads a minimal operating system.
-   It begins the installation process from a shared folder on the server containing the installation files.

You can also use internet-based client management (IBCM) to install Windows on clients that are not connected to an internal network

#### Recovery Drive
If you have created a recovery partition on a PC, you can use it to recover a PC that won’t start up correctly. When booting from a recovery partition, you’ll get options to reset or see advanced options. These include the options to:

-   **Try a system restore.** A system restore won’t affect personal files. It will, however, remove any recently installed apps or updates to discover what is causing problems.
-   **Recover from a drive.** This option reinstalls the Windows operating system. It will remove all user files, apps, configurations, and drivers.

### Installation Process
#### Insert Installation media
- Insert (or connect to the installation media) and boot from that media.
#### Load Files
- During the first part of the installation, Windows loads the necessary files it needs to start the installation. During this phase, you may need to load additional drivers to support the storage controller so that Windows can write to the disk. To do this, select **Load Driver**. You must have the necessary drivers available on a USB flash drive.\
#### Partition and format drive
- After the initial files and drivers are loaded, select the disk where you want to install Windows. You can choose an existing partition (if one exists) or choose to have the installer create and format a partition for you.
#### File copy
- After Windows prepares the disks, it starts copying files to the hard disk. When the file copy is complete, the system reboots. Leave the installation media in the drive until prompted to remove it.
#### Configuration
- After the system reboots, Windows configures the system. You will be prompted to verify and configure various settings including such things as country or region, keyboard layout or input method, and device name.

## 6.2.10 Post-Installation Facts
### Complete the following tasks
#### Configure the boot order
- Edit the BIOS/UEFI settings to boot from the hard drive first. This prevents the system from accidentally booting from the installation media.
#### Activate Windows
Activate Windows with a valid digital license or a 25-digit product key. If you opted not to activate during the installation process, Windows sends an Activate Windows reminder until the activation has been completed. You can check the activation status under Windows Settings at any time.  
  
After installation, you can activate the Windows 11 system as follows:

1.  Right-click **Start** and select **Settings**.
2.  Select the appropriate response:
    -   For Windows isn't activated, select **Activate now**.
    -   For Change product key, select **Change**.
3.  Enter the product key and follow the remaining prompts.
#### Configure Windows Update
- Configure Windows Update and download the latest updates. You can check for recent updates by accessing Settings > Windows Update > **Check for Updates**.
#### Configure anti-malware
- Use Windows security and/or install and configure any third-party firewall, anti-malware, and anti-virus software applications.
#### Configure user environment
Manage user configuration settings and data. You can:
-   Add or remove the apps and folders that display on the Start menu to provide users with the tools they need to do their jobs.
-   Configure the taskbar to allow users quick access to the tools they need without cluttering the desktop.
-   Configure the desktop environment (such as the background and lock screen) according to the organization's policies.
-   Activate and configure Cortana.
-   Configure accessibility options to support users who have vision, hearing, interaction, or other physical limitations.
#### Complete Documentation
- Record as much information as you can about the system. This could include computer make and model; purchase date; vendor and warranty information; Windows version and edition; product key; installed applications; etc.