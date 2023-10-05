
---
aliases: [ "20230217142142",  ]
tags: SEC.101, SEC, PCPro
date_created: 2023-02-17 14:21
---
[[SEC.101 Index]]
# TestOut PC Pro - 5.7
---
## 5.7.3 Storage Space Facts
- This lesson covers the following topics:
	- Storage Spaces overview
	- Storage Spaces benefits
	- Drive Use

### Storage Spaces Overview
_Storage Spaces_ is a technology that allows you to pool space from multiple disk drives (or other storage devices) to create one or more logical drives. The logical drives display in File Explorer for storing data and other user files. A storage space appears to the user as one drive regardless of the number of disks or devices contributing space to the storage pool.
- Not available in windows 7

Storage spaces are comprised of three components:
- _Devices_ are the hard disks or other types of storage from which storage pools are created. You can use a variety of devices such as SATA drives and external drives to create storage pools.
- Pools of storage are created from the available disk space. A _pool_ is a logical concept composed of the free space available on the specified storage devices.
- A _storage space_ defines a logical unit of space created from a pool. One or more storage spaces can be created from the pool. To the Windows system and the user, storage spaces appear as disks with typical drive letters (e.g., E: drive, F: drive).

### Storage Space Benefits
#### Ease of Adding Space
Storage spaces eliminate the need for such tasks as repartitioning drives, resizing volumes, and backing up data in order to repartition. When you need more disk space for a storage space, follow these steps:

-   Install a new storage device to the system.
-   Add the free space on that device to a storage pool.
-   Allocate space to an existing storage space.

#### Data Resiliency
Storage spaces can include data resiliency. Choosing an option that provides resiliency requires you to allocate space for redundant information. The options for storage spaces data include:

-   Simple, which does not provide redundancy.
    -   This option adds space from the storage pool to the storage space.
    -   When you select the Simple option, all the data in the storage space is lost if one of the drives fails.
-   Two-way mirror requires at least two storage devices.
    -   The data is written to two devices.
    -   Two-way mirror requires twice as much device space as the amount of storage allocated to the storage space.
    -   This option protects you from a single storage device failure.
-   Three-way mirror requires at least five storage devices.
    -   The data is written to three storage devices.
    -   This option provides redundancy for the data if two storage devices fail at one time.
-   Parity provides resiliency by writing parity information across the physical disks using bitwise arithmetic. It requires at least three drives to protect you from a single drive failure and at least seven drives to protect you from two drive failures.
    -   This option uses parity information to reconstruct data if one of the storage devices fails.
    -   Parity uses less space for redundancy than the mirror options, but performance is not as good as the mirror options if a device failure occurs.
    -   Parity spaces are best for archival data and streaming media, like music and videos.
    -   Parity requires only 50 percent more redundancy space than storage space.

#### Thin Provisioning
Thin provisioning (also called overbooking) allows you to allocate larger storage spaces than the disk space available in the pool.

-   Thin provisioning is based on the premise that not all users will use all of space in their allocated storage space.
-   Space is added to a user's storage space as the user consumes space.
-   If a storage space runs out of disk space, it will immediately unmount, leaving any I/O processes vulnerable to data corruption.
    -   An unmounted storage space must be brought back online manually.
    -   Files can be accessed after the storage space is brought back online manually, but you must add more physical disk space to the pool and add it to the storage space in order to use the storage space.

### Drive Use
To use drives properly, you must know how to initialize a drive, check a drive status, split partitions, shrink partitions, and assign drive letters. The following table describes these tasks.

#### Initialize a drive
- You can initialize (format) a new hard drive disk on a Windows system from Disk Management.
#### Check a Drive Status
A drive status message indicates whether a drive is available. You can use a variety of command tools and applications to check drive status.

-   Depending on the tool, an available drive might be labeled UP, Okay, Good, or a similar label.
-   An unavailable status may be labeled DOWN or Bad.
#### Split Partitians
To split a partition in Windows 10, download and install the EaseUS Partition Master program. From the program interface, you can split a partition and reallocate space.
#### Shrink Partitians
You can shrink a partition in Disk Management using the Shrink Volume option in Computer Management.
#### Assign Drive Letters
When you connect a new drive to a PC, Windows automatically assigns the next available drive letter after C.

-   Change the drive letter from Disk Management using the Change Drive Letter and Paths option.
-   Use a letter other than A or B, which were historically reserved for floppy drives and can confuse older software.
