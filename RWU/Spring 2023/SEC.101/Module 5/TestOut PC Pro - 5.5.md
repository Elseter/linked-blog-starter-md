
---
aliases: [ "20230216142608",  ]
tags: SEC.101, SEC, PCPro
date_created: 2023-02-16 14:26
---
[[SEC.101 Index]]
# TestOut PC Pro - 5.5
---
## 5.5.3 File System Facts
This lesson covers the following topics:
- File system components
- Formatting
- NTFS
- Extended File Allocation Table (exFAT)

### File System Components
A file system organizes and stores data and information on a storage device. 
- The file system and the operating system work together to ensure data availability, integrity, and accessibility.

#### Partition
- a partition is a logical division of a storage device
	- before partition, must be initialized
	- partition style is selected
		- Master Boot Record (MBR)
		- GUID Partition Table (GPT)
- A single device can contain multiple partitions
- can be created without formatting but requires formatting to be installed or to store data
- given a drive letter
- cannot span to a separate physical storage device
##### Reasons to partition
- Assigning the boot system to a different partition than application and data files can help many computers run more smoothly and minimize damage in a system crash.
- Storing the swap file on its own partition is sometimes necessary or useful.
- Creating a separate partition for the operating system can help it run properly. Some operating systems can't run on a large partition.
- Assigning log files to be stored on distinct partitions can help minimize the effects of a system crash caused by excessively large log files.
- Assigning distinct operating systems to run on separate partitions allows a multiple boot system setup.

- Unallocated space is space on a partition that has not been assigned to a volume
	- cannot store or read data

#### Volume
- is a single accessible storage area within a file system
- can be a single partition or multiple partitions 
- defined by drive letters

#### Directory
- also called a folder
- container in a volume that holds files or other directories
- use it to logically sort and organize data
- most OS use hierarchal filing structure

#### File
- A file is a one dimensional stream of bits treated as a logical unit
	- most basic component of file system
		- organize raw bits of data
	- file name is made up of directory path and file name
	- An extension can also be added to the filename to identify the file type and the program used to create, view, and modify the file

### File Systems
- Common ones (other than exFAT, FAT32, and NTFS) include:
	- Compact Disk File System (CDFS) - A virtual file system used with Linux.
	- Network File System (NFS) - A distributed file system that allows client computers to access files over a computer network.
	- Ext4 - The default Linux file system (and its predecessor ext3, which is still in use).

### Formatting
- the process of preparing a partition to use a specific file system
	- When you format a disk, you identify the file system type and identify the cluster size used to store data.
	- Reformatting removes the existing file system and replaces it with the new file system type. Reformatting a drive deletes all existing data.
	- If your system or disk supports multiple operating systems, be sure to select a file system supported by all operating systems you will use.
	- Microsoft does not recommend the use of NTFS on a volume that is smaller than approximately 400 MB (due to the amount of space overhead involved in NTFS).
	- When using NTFS on removable devices, you must use the Safely Remove Hardware feature before removing the flash device to prevent file corruption.
	- A Full format removes the files from the partition. The hard disk is also scanned for bad sectors.
	- A Quick format removes the reference (or index) to the files, but the files are still there. Because the reference to the files has been deleted, the files are inaccessible. The disk is not scanned for bad sectors.

|        Property         | FAT32                               | NTFS                                |
|:-----------------------:| ----------------------------------- | ----------------------------------- |
|     Partition Size      | 2 terabytes*                        | 256 terabytes                       |
|       Volume Size       | 2 terabytes*                        | 256 terabytes                       |
|    File name length     | Long File names (255 chars, spaces) | Unicode (255 chars, anything but /) |
|        File size        | 4 gigabytes                         | 16 terabytes                        |
| Number of Files allowed | 268,435,437                         | 4,294,967,295                       | 
- to create a FAT32 partition bigger than 32 GB, you need to use command prompt, PowerShell or a third-party tool

#### NTFS
- in windows, you typically choose NTFS over FAT to take advantage of additional features
	- The ability to format larger partition sizes in Windows.
	- Smaller cluster sizes for more efficient storage with less wasted space.
	- File and folder permissions to control access to files.
	- Encryption to hide the contents of a file.
	- Compression to reduce the amount of space used by files.
	- Disk quotas to restrict the amount of disk space that files saved by a user can use.
	- Volume mount points that allow you to map disk space on another partition into an existing volume.

#### exFAT
- Sometimes called FAT64
- a special file system that is designed to support large flash drives
- Using NTFS on flash drives is usually not a good idea due to its high overhead and risk of corruption if the device is not stopped properly prior to removal
- However, many flash drives are now larger than 32 GB so exFAT was introduced

## 5.5.5 MBR Partitioning Facts
- This lesson covers the following topics:
	- Disk Partitioning
	- Disk management items

### Disk Partitioning 
- logical division of the storage space on a hard disk drive
- Partitions are identified by 16-bit entries that make up the partition table located in the master boot record (MBR) of the drive 
- A hard disk can contain a single partition that encompasses the entire drive or multiple partitions that divide up the storage space on the hard disk drive.

Windows supports two kinds of disks, **basic** and **dynamic**. The disk type controls characteristics about how partitions and volumes are defined.

#### Basic Disk Drives
- Use primary and extended partitions.
    - Each physical disk can have up to four primary partitions or three primary partitions and one extended partition.
    - Logical drives are defined within an extended partition. You can have up to 24 logical partitions on an extended partition. The extended partition can be divided into multiple logical drives.
- Require a logical drive in an extended partition before you can format and store data. The logical drive is the storage unit, not the partition.
- Are supported by all operating systems.
- Support only volumes made up of contiguous disk space.
- Store partition information in a portion of the master boot record (MBR) known as the partition table.
    - The partition table has room for up to four partition entries.
    - When you use an extended partition, one of the four entries points to an extended boot record (EBR). The EBR is located within the extended partition and contains information about the logical drives within the extended partition.

#### Dynamic Disk Drives
Dynamic disks have the following characteristics:
- Volumes on dynamic disks are like partitions and logical drives on basic disks.
- Dynamic disks support up to 128 volumes.
- Dynamic disks support volumes that use noncontiguous disk space.
- Simple volumes contain disk space from a single hard disk (either contiguous or noncontiguous space).
- Spanned volumes contain disk space from multiple hard disks grouped as a single logical volume.
- Dynamic disks store partitioning information in a hidden database on all dynamic disks in the system.

### Disk Management Items
Be aware of the following when managing partitions and volumes:
- You should use Disk Management or DiskPart to create, format, and manage partitions and volumes.
    - Access Disk Management on Windows systems through Computer Management.
    - Access DiskPart from the Command Prompt or Windows Terminal.

- Basic and dynamic disks use the same hardware, but different partitioning methods.
- You can convert a basic disk to a dynamic disk without losing data in existing partitions.
    - Existing basic volumes and logical drives in an extended partition are converted to dynamic volumes.
    - You must reboot the system to complete the conversion if the disk contains the boot or system volume, or if the volume includes the page file.

- When converting from a dynamic disk to a basic disk, you must delete all existing volumes.
- The active partition identifies the partition that contains the operating system (or the program that loads the operating system) used to start the computer.
- The extended partition or a logical drive on the extended partition cannot be set to active.
- You cannot install the operating system on a dynamic disk. You can, however, upgrade a basic disk containing the operating system to a dynamic disk after installation.

- When you shrink a partition, unmovable files (the paging file or the shadow copy storage area) are not automatically relocated.
    - You cannot decrease the allocated space beyond the point where the unmovable files are located.
    - To shrink the partition further:
        - Check the Application log for Event 259. It identifies the unmovable file.
        - Move the paging file to another disk.
        - Delete the stored shadow copies.
        - Shrink the volume.
        - Move the paging file back to the disk

- You can shrink primary partitions and logical drives on raw partitions (those without a file system) or partitions using the NTFS file system.
- To shrink a partition, you must be a member of Backup Operators or Administrators (or equivalent) to complete this process.

## 5.5.7 GPT Partitioning Facts
- This lesson covers the following topics
	- GUID Partition Table (GPT) partitions
	- GPT implementation concerns

### GPT Partitions
- newest partitioning style
- now the default option when initializing a disk
- GPT is associated with Unified Extensible Firmware Interface (UEFI)
- The name GPT is based on the fact that every partition on the drive has a globally unique identifier (GUID). 
	- That means that each partition worldwide would have its own unique identifying number.

- **A GPT Partition**:
	- Can be configured as a basic disk or a dynamic disk.
	- Supports up to 128 partitions depending on space allocated for the partition table. There is no need for extended and logical partitions.
	- Can support between 8 and 9.4 zettabytes depending on the sector size.
	- Stores multiple copies of the partition table across the disk. GPT partitions:
	    - Are more robust than previous partition types.
	    - Can recover if the data is corrupted.
	- Stores cyclic redundancy check (CRC) values to check that data is intact.
	    - If the data is corrupt, GPT notices the problem and attempts to recover the damaged data from another location on the disk.
	    - The master boot record (MBR) doesn't know if the data is corrupted. You would know there was a problem only when the boot process failed or the partitions vanished.
	- Includes a protective MBR.
	    - The protective MBR sees the GPT drive as a single partition that extends across the entire drive.
	    - If you try to manage a GPT disk with an old tool that can only read MBRs, it will see the GPT disk as a single partition that extends across the entire drive.
	    - The protective MBR makes sure that the old tools don't mistake the GPT drive for a non-partitioned drive and overwrite all the data.

### GPT Implementation Concerns
- You should be aware of the following
	- You should use the GPT partition style whenever possible. However, if you need compatibility with old systems, like the ability to boot Windows off a drive on a computer with a traditional BIOS, you'll need to use MBR.
	- Windows can boot from GPT only on UEFI-based computers running 64-bit versions of Windows 7 or newer, and the corresponding server versions.
	    - All versions of Windows 7 and newer can read GPT drives and use them for data, but they cannot boot from them without UEFI.
	    - Because Windows 7 does not support UEFI on 32-bit platforms, you cannot boot from a GPT partition on Windows 7.
	- Linux has built-in support for GPT.
	- Apple's Intel Macs no longer use the Apple Partition Table (APT) scheme but use GPT instead.

## 5.5.13 Disk Status Facts
- The following describes various disk and volume statuses that you might encounter in Disk Management
### Healthy or Online
- Indicates the disk is turned on and can be accessed. The volume on the disk is valid and has no errors.
### Formatting
- Is shown for volumes during the formatting process. After formatting is complete, the status for the volume changes to Healthy.
### Unallocated
- Is shown when portions of a disk have not been assigned to a partition or a volume.
### Initializing
- Is shown while a disk is being converted from a basic disk to a dynamic disk. After the conversion, the status for the volume changes to Healthy.
### No Media
- Is shown for an optical or removable media drive that does not contain a valid disc. This disk status applies only to CD-ROM, DVD-ROM, or removable disks.
### Foreign
- Is shown for a foreign disk. A _foreign disk_ is a dynamic disk that was created in one system and moved to another system. When you first add the disk to a different system, the partition information for the disk must be updated to reflect all dynamic disks in the current system. Import the disk to make it available in the new system.
### Not Initialized / Unknown
- Indicates a disk without a valid master boot record or a missing or corrupt partition table. To correct the problem, initialize the disk. If the partition table is invalid, use third party tools to try to recover the partition table.
### Online (Errors)
- Indicates that I/O errors are detected on a dynamic disk. To correct the problem, try reactivating the disk.
### Unavailable
- Indicates that errors occurred on physical or dynamic disks.
### Unreadable
- Indicates a hardware failure, I/O errors, or other corruption. Can also be caused by a delay in reading the disk in Disk Management. Try rescanning the disk to see if the status changes. If it doesn't, troubleshoot the hardware or disk.
### Missing or Offline
- Is shown when a dynamic disk has failed, been removed, or turned off. If the disk is turned off, turn it on, and reactivate the disk. If the disk no longer exists, delete the disk from Disk Management.
### Failed
- Is shown for a volume that cannot be started, such as when the disk is damaged or the file system is corrupt. Make sure the disk is on and try reactivating the volume. If that doesn't work, then you likely have data loss.

