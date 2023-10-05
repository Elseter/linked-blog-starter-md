
---
aliases: [ "20230125133731",  ]
tags: SEC.101, PCPro, SEC
date_created: 2023-01-25 13:37
---
[[SEC.101 Index]]
# TestOut PC Pro - 4.2
---
## Windows Basics
### Windows Operating System Facts 4.2.2
#### How an Operating System Works
>[! def] Operating System
>An operating system is a set of programs that act as an interface between applications that are running on a computer and the computer's hardware.
- They often preform actions such as:
	-   Receive user input from devices such as the keyboard or mouse.
	-   Send user output to devices such as the monitor or a printer.
	-   Control processing devices by applications.
	-   Serve as a platform for applications.
	-   Moderate hardware.
	-   Provide security.
	-   Manage the file system.

#### Operating System Attributes
- `multiprocessing` - the ability to use multiple processing units (CPUs) in a single system
- `multitasking` - the ability to run multiple application simultaneously 
	- `Cooperative multitasking` - requires multiple processes to work together for the operating system to work effectively
	- `Preemptive multitasking` - forces applications to share the CPU
- `Multithreading` - the ability to run multiple parts of an application simultaneously 

#### Operating System Components
|  Component  | Description                                                                                                                                                                       |
|:-----------:| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|   Kernel    | The core of the operating system. It is loaded into memory when the computer boots. It controls security, manages the file system and provides a platform for applications to run |
|   Driver    | A type of computer program that enables the operating system to interact with hardware devices                                                                                    |
|  Interface  | An interface allows the user to interact with the kernel and utilities. There are two main types. Command Line and Graphical User Interfaces                                      |
|  Utilities  | Utilities are features or programs included with an operating system that preform system-related tasks. Common Windows Utilities are settings, Disk Management and computer management                                                                                                                                                                                    |
| Application | A subclass computer program designed for end users                                                                                                                                                                                  |

### Windows Editions 4.2.5
#### Windows 10 Editions
##### Windows 10 Home
-   Intended for home use.
-   Offers the most basic features.
-   Includes safety features:
    -   Device encryption
    -   Firewall and network protections
    -   Windows Defender antivirus
    -   Windows Hello authentication
    -   Secure Boot
    -   Internet protection
    -   Parental controls
-   Includes fundamental features:
    -   Battery saver mode
    -   Mobile function for connecting to mobile devices
    -   Microsoft Edge browser
    -   Voice for hands-free functions
    -   Digital pen and touch

##### Windows 10 Pro
-   Intended for business professionals.
-   Offers all Home edition features plus:
    -   BitLocker device encryption
    -   Windows Information Protection (WIP)
    -   Mobile device management
    -   Windows update for business
    -   Microsoft Store for Business
    -   Support for Active Directory and Azure Active Directory
    -   Group Policy
    -   Assigned Access
    -   Dynamic provisioning
    -   Enterprise State Roaming with Azure
    -   Hyper-V

##### Windows 10 Pro for Workstations
-   Intended for business professionals whose work requires high-end hardware for intense computing, with fast data processing and large storage capacity. Examples include: CAD engineers, graphic designers, medical scientists, and media producers.
- Offers all Pro edition features, plus:
    - Resilient file system (ReFS)
        -   Fault-tolerant storage
        -   Auto-correcting
        -   Cloud-based
    - Persistent memory
        -   Non-volatile memory modules (NVDIMM-N)
        -   Fast reading and writing of files
        -   Data saved in memory, even when powered down
    - SMB Direct
    - Capacity to use Intel Xeon or AMD Opteron
    - Capacity of up to 4 CPUs
    - Capacity of up to 6 TB of memory
##### Windows 10 Enterprise
-   Intended for large organizations that have IT professionals managing the systems.
-   Requires a volume licensing agreement.
-   Offers all the features of the Pro edition plus the following features:
    -   Credential Guard
    -   Application Guard
    -   Application Control
    -   Advanced Threat Protection (ATP)
    -   Device Guard
    -   Direct Access
    -   User Experience Control
    -   Microsoft Application Virtualization (App-V)
    -   Microsoft User Environment Virtualization (UE-V)

##### Windows 10 Hardware Requirements
-   1 GHz processor with support for PAE, NX, and SSE2
-   1 GB RAM (2 GB for a 64-bit system)
-   16 GB free disk space (20 GB for a 64-bit system)
-   DirectX 9 graphics device with WDDM driver
-   DVD-ROM drive (if installing from a DVD)
>[! tip] Supported Until
Microsoft will support Windows 10 until October 14, 2025.

#### Windows 11 Editions
- The Windows 11 is designed to be more user-friendly. It is also designed for a more hybrid working environment that can go from home to work, even if the transition is in the same home office.
##### Windows 11 Home
- Intended for home use.
- Offers Windows 11 most basic features.
- Includes fundamental features such as:
    -   Snap layouts
    -   Desktops—for grouping and easily changing desktop groups
    -   Microsoft Teams—for communicating with others through chats and video conferencing
    -   Widgets—accessible from taskbar and customizable
    -   Enhanced gaming features
    -   Microsoft Edge
    -   Microsoft Store
    -   Touch, Pen, and Voice features
- Includes security features such as:
    -   Device encryption
    -   Find my device
    -   Firewall and network protection
    -   Internet protection
    -   Secure Boot
    -   Windows Security
    -   Windows Hello
    -   Parental controls

##### Windows 11 Pro
- Intended for business professionals.
- Offers all Home edition features plus:
    -   BitLocker device encryption
    -   Windows Information Protection (WIP)
    -   Assigned Access
    -   Dynamic Provisioning
    -   Windows Update for Business
    -   Support for Active Directory and Azure Active Directory
    -   Mobile device management
    -   Group Policy
    -   Microsoft Store for Business
    -   Enterprise State Roaming with Azure
    -   Kiosk mode setup
    -   Hyper-V

##### Windows 11 Pro for Workstations
- Intended for business professionals whose work requires high-end hardware for intense computing, with fast data processing and large storage capacity. Examples include: CAD engineers, graphic designers, medical scientists, and media producers.
- Offers all Pro edition features plus:
    - Resilient file system (ReFS)
        -   Fault-tolerant storage
        -   Auto-correcting
        -   Cloud-based
    - Persistent memory
        -   Non-volatile memory modules (NVDIMM-N)
        -   Fast reading and writing of files
        -   Data saved in memory even when powered down
    - SMB Direct
    - Capacity to use Intel Xeon or AMD Opteron
    - Capacity of up to 4 CPUs
    - Capacity of up to 6 TB of memory

##### Windows 11 Enterprise
- Intended for large organizations who have IT professionals managing the systems.
- Requires a licensing agreement.
- Is part of Microsoft 365 Enterprise.
- Offers all Pro edition features plus:
    -   Credential Guard
    -   Application Guard
    -   Application Control
    -   Advanced Threat Protection (ATP)
    -   Device Guard
    -   Direct Access
    -   User Experience Control
    -   Microsoft Application Virtualization (App-V)
    -   Microsoft User Environment Virtualization (UE-V)
- Offers options within the Enterprise editions including:
    -   Windows Enterprise E3
        -   Intended for mid-size to large organizations.
        -   Includes all Windows 11 Pro features plus:
            -   OS deployment and update control options
            -   Device and application management features
            -   Serverless print management and Universal Print
            -   Added security protections
- Windows Enterprise E5
    -   Intended for organizations that want to use cloud-delivered endpoint security.
    -   Includes all Enterprise E3 features plus Microsoft Defender for Endpoint
- Windows Enterprise E3 in Microsoft 365 F3
    -   Intended for mid-size to large organizations with frontline workers.
    -   Includes all Enterprise E3 features.

##### Windows 11 minimum hardware requirement
- 1 GHz or faster processor with at least two cores on a compatible 64-bit processor or SoC
- 4 GB RAM
- 64 GB storage
- UEFI, Secure Boot capable firmware
- Trusted Platform Module 2.0
- DirectX 12 or later with WDDM 2.0 driver graphic card
- 720p, 8-bit per color channel, 9-inch diagonal or greater display

#### Windows 10 Features no longer in Windows 11
-   People —contacts can no longer be pinned to the taskbar
-   Skype —no longer standard with Windows OS
-   Timeline —no longer able to resume activities and files from a previous session
-   Cortana —no longer enabled by default, but can be enabled if desired
-   Internet Explorer —removed; Windows 11 uses Microsoft Edge
-   S mode —now available only in Home edition
-   Tablet mode —removed
-   Wallet —removed

### Windows Features 4.2.7
#### Management and Security Features
##### Domain Access
Accessing a domain through a domain account is a **good option for large networks.**  
How a domain network works:
- You can divide users who have the same privileges and access rights into groups.
- Control is through a domain controller.
    - A domain controller is a server that handles authentication requests and enforces security policies.
    - Domain controllers store user account information in a centralized storage database.
- You can use domains to securely transfer or share data.
- You can use domains to manage computers within the domain network. Changes made in the domain are automatically applied to all computers within the domain.
- Computers on local networks can be part of the same domain.
- Logging on to the domain gives access to all the domain resources.

##### Workgroup
Workgroup accounts are for **small networks on a local network**. How workgroups work:
- All computers are peers to each other. There isn't a central administrator.
- Each device has its own storage.
- The user manages the device.
- A user must have an account on the device to log on to it.
- Workgroups allow users to share files, printers, and local network resources.
- Workgroups usually consist of twenty or fewer computers.

##### Group Policy Editor  (gpedit.msc)
The Group Policy Editor is a graphical snap-in for Windows settings stored in the registry. It:
- Provides a simplified GUI for changing settings in the registry.
- Contains more than 3,000 Windows settings to choose from.
- Allows you to centrally configure and enforce settings on all computers in an Active Directory network.
- Uses the domain controller to implement the settings in an Active Directory network.
- Can also be used on a small scale for enforcement of restrictions or to run specific scripts at specified times.

##### BitLocker
BitLocker is Microsoft's whole disk encryption feature. It:

- Is available on Pro and Enterprise editions.
- Creates a recovery key that is used to access the encrypted hard drive.
- Is designed to protect computers if lost or stolen.
- Primarily uses a Trusted Platform Module (TPM) as part of the encryption process.
    - TPM is a hardware chip often installed on newer computers by the manufacturer.
    - TPM is a crypto-processor that creates and stores cryptographic keys.
    - TPM is used for authentication.
- Allows you to encrypt entire disk or just the data.
    - Encrypting just the data is a faster process.
    - Encrypting the entire hard drive is more secure.

#### User Features
##### User Interface Customization
You can customize the user interface and desktop styles. Settings you can use to personalize the user interface include:
-   Background
-   Colors
-   Themes
-   Transparency effects
-   Taskbar items and location
-   Start menu items
-   Fonts

##### Random Access Memory (RAM) limitations
-   Home edition supports up to 128 GB of RAM.
-   Pro edition supports up to 2 TB of RAM.
-   Pro for Workstations edition supports up to 6 TB of RAM.
-   Enterprise editions support up to 6 TB of RAM.

##### Remote Desktop Protocol
RDP is a Microsoft protocol that allows remote access to a Windows machine. It:
- Is available on all editions except the Home edition of Windows.
- Allows a remote user to see and manipulate the machine through an encrypted exchange.
- Can expose the machine to cyber attacks. It's a best practice to implement additional security protocols when enabling RDP.

### Windows Interface 4.2.10
#### Interface Components 
##### Desktop
The _desktop_ is the working surface that contains icons you can use to access programs, files, applications, and file systems. The desktop is what you see when all programs and open folders are minimized. Installing an application often adds an icon to the desktop.

##### Start Menu
-   At the top is a search field you can use to search for a known application.
-   Below the search field are apps pinned for quick access.
    -   You can customize the order of the pinned apps.
    -   You can add and remove pinned apps from the Start menu.
-   In the top right corner, you can select All apps to list all applications on the computer in alphabetical order.
-   You can right-click an app in the list and pin or unpin it to the start menu.
-   You can uninstall apps from the Start menu.
-   You can change account settings, switch users, or lock the desktop from the profile section of the Start menu.
-   Power options and advanced features are available in the bottom right corner. Right-click the Start button to access the advanced features for OS management.

##### Taskbar
-   Allows you to move it to the left or leave it centered on the screen.
-   Displays the icons of apps currently running or pinned to the taskbar. You can:
    -   Access a running app by clicking the app's icon.
    -   Launch a pinned app by clicking the app's icon.
-   Can be hidden.

##### Settings App
-   Has a search bar at the top for quick location of a desired setting.
-   Retains a category list on the left side of the page regardless of the page selected.
-   Displays breadcrumb navigation at the top when accessing categories.
-   Has updated visual icons.
-   Contains features added from the Control Panel. For example:
    -   Advance sharing settings (Network discovery, public folder sharing, and file and printer sharing).
    -   Advanced network settings.
    -   Printers & Scanners pages.
    -   Entry points for network and device settings.
-   Recommends settings based on configuration selections.

##### Virtual Desktop
-   Can be toggled from one to another from the taskbar.
-   Allow you to run multiple programs separately on different virtual desktops.
-   Allow each desktop to have a unique background to help distinguish it.

##### Widgets
-   Local weather.
-   Trending news.
-   Options to add more widgets such as to do lists or Outlook calendar.
-   Options to personalize news feed and interests.
-   An option to remove it from the taskbar.

##### Chat
The Chat icon on the taskbar syncs contacts on Windows or from a mobile device to Microsoft Teams. It allows the user to make video calls or chat with contacts through a Microsoft account.

#### What's New With Windows 11
-   A cleaner user interface with updated design.
-   Snap layouts that let you select layouts, grouping, and organization options for working with multiple pages on the screen simultaneously. Layout/grouping options vary depending on screen size. To use snap layouts:
    -   Hover over the minimize icon to select the layout.
    -   Hover over the desktop icon on taskbar to navigate between layouts.
-   The redesigned Microsoft Store which offers Windows 11 and Windows 10 apps, as well as Android apps hosted on the Amazon App Store.
-   Teams (replaces the Skype options) to offer chat and video calls with contacts.
-   Larger touch targets and visual prompts for tablet users.
-   Virtual desktops for organizing applications by topic or work environment.
-   Auto high dynamic range (HDR) which expands the range of colors in many DirectX games and other newer games.
-   Faster Windows Hello logon.
-   Faster download time for Windows updates.

### Windows Upgrade 4.2.12
>[! tip] Upgrades Types
>`In Place Upgrade:` the installation of the Windows operating system without removing the existing operating system and without having to save the data. With an in-place installation, the user data and applications remain intact through the upgrade process.
>
>`Clean Install:` With a clean install you must externally save all user data and reinstall it after the OS installation. Also, you must reinstall all applications after a clean install.

#### Common In-Place Installation Methods
- These may be a good option when the windows operating system is behaving strangely
- This process replaces any corrupted system files without losing the user data or applications
##### Windows Update
- This works when upgrading from an older version of Windows to a newer version, such as Windows 10 to Windows 11.
- You cannot use Windows Update if there are multiple versions released between the current OS and the desired upgrade. For example, you cannot upgrade to Windows 11 from Windows 7.
- To use this method, go to Settings > Updates and Security > Check for updates.
- If the update is available, click Download and install
>[! bug] Doesn't always work
>You may not always be given this option, even if your computer is a valid candidate

##### Installation Assistant 
- Sign in with admin privileges.
- Disable third party antivirus software.
- Perform a backup of data. (Even though no user data should be lost, backing up data is always a best practice).
- Unplug all peripheral devices except the mouse and keyboard.
- Plug into an Ethernet cable or a LAN cable (if possible) to ensure connectivity to the internet throughout the upgrade process.
- Go to the Microsoft site and download the PC Health Check app.
- Go to Microsoft website's Software Download page and click **Download Windows 11 Installation Assistant**.
- Run the PC Health Check app. If needed, make the required changes so that the computer is compatible with Windows 11.
- Run the Windows 11 Installation Assistant and select **Accept and install**.
- When the installation is complete, the computer will automatically restart in 30 minutes, unless you select **Restart Later**.
- Restart the computer.

##### ISO Installation Media
The advantage of using this method is that the upgrade performs more quickly from the downloaded file. This is very advantageous if you are upgrading several computers, since you need to download the software only once. It also gives you the ability to upgrade a system that does not have access to the internet or the connection to the internet is very slow.  
  
To perform the in-place upgrade, the system to be upgraded must be powered on, running Windows, and have access to the Windows 11 ISO file. This can be done in two ways:

-   Copy the Windows 11 ISO media to a Windows 10 machine.
-   Copy the Windows 11 ISO to a bootable installation media such as a USB flash drive or DVD.

To perform an in-place upgrade from an ISO file, complete the following:

1.  Right-click the Windows 11 ISO file and select **Mount**.
2.  Wait for the ISO file to mount.
3.  Right-click setup.exe and select **Run as administrator**.
4.  Follow the prompts as directed.

##### System Center Configuration Manager (SCCM) Task Sequence
The SCCM task sequence method is an option if you are currently manually deploying operating systems and managing software updates through the Configuration Manager. To install using the SCCM:

-   Import or add Windows 11 upgrade package into SCCM.
    -   Open the SCCM console.
    -   Go to Software Library > Operating Systems > Operating System Upgrade Packages.
    -   Right-click **Operating System Upgrade Packages**.
    -   Click **Add Operating System Upgrade Packages**.
-   On the Data Source window, select **Browse**.
-   Select the Windows 11 setup file folder path.
-   Click the boxes to accept the terms.
-   Click **Next**.
-   Select the General window.
-   Name the upgrade package: Windows 11 Upgrade.
-   Click **Next**.
-   Click **Next** again on Summary window.
-   Click **Close** on the Completion window.

#### SetupDiag Diagnostic Tool
If an in-place upgrade fails, you can use the SetupDiag diagnostic tool to determine the cause of the failure. You can run the tool on the computer that failed the upgrade, or in an offline mode on another computer using logs exported from the computer that failed to upgrade.

SetupDiag facts:
-   SetupDiag is included with Windows Setup on Windows 10, version 2004 and newer.
-   When included, the tool will run automatically if a failure occurs in the upgrade process.
-   If the diagnostic results show multiple failures, typically the last failure listed is the fatal error.
-   If you have a Windows version earlier than Windows 10, version 2004, you can download and use SetupDiag to find the cause of an upgrade failure.