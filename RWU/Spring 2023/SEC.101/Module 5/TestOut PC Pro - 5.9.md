
---
aliases: [ "20230219164306",  ]
tags: SEC.101, SEC, PCPro
date_created: 2023-02-19 16:43
---
[[SEC.101 Index]]
# TestOut PC Pro - 5.9
---
## 5.9.2 Storage and RAID Troubleshooting 
This lesson convers the following topics
- Resource troubleshooting
- Storage drive types
- Common storage issues
- Redundant array of independent disks (RAID) troubleshooting

### Resource troubleshooting
Several commonly observed issues with storage devices are discussed in this lesson. Be aware that this lesson cannot cover every storage issue and its cause. Instead, more common issues and their causes are addressed. For more complex issues, use all the resources available in order to identify the problem. This includes the following:
-   System docs
-   Knowledge bases
-   Service manuals
-   User forums

### Storage drive types
When troubleshooting storage drives, it is important to know the type of drive you are working with. There are two main types of storage drives that are used in computers: mechanical hard disk drives (HDDs) and solid-state hard drives (SSDs).
	- Mechanical hard disks have moving parts that wear out over time. It's not a matter of if an HDD will fail, it's a matter of when it will fail.
	- SSDs don't have any moving parts, but the storage medium they use has finite read/write counts. The more use an SSD gets, the faster it will wear out.

All storage devices have a mean time between failure (MTBF) rating that is an estimated lifespan for the device. 
- Because storage devices are sealed, there's no physical maintenance you can perform on them. Instead, you need to decide when it is time to replace the disk. 
- Accordingly, you should implement a data backup plan to protect the data on for hard disks in the event of a failure.

### Common Storage Issues
#### HDD
##### Slow Performance
- To help increase the performance of a slow HDD:
	- Maintain a healthy amount of free disk space on the drive. A mostly empty disk runs faster than a mostly full disk. If a disk is getting full, migrate to a newer, bigger disk.
	- Keep the disk defragmented. A heavily fragmented disk can run quite slowly. You need ample free space to fully defragment the drive.
	- Check the disk rotational speed. A disk that spins faster will perform better.
	- Check the speed of the disk interface. If the system uses an older disk interface, upgrade to a faster interface (if possible).

##### Failure to Boot (SAME FOR SSD)
- A failure to boot with an error message that reads OS Not Found (or something to that effect) could be trivial or serious. Common causes include the following:
	- The disk you're booting doesn't have an operating system installed. This is a very common issue.
	    - The error frequently occurs when a CD or DVD is in the optical drive at system boot and the BIOS/UEFI is configured to boot from the optical drive first. The error message displays when an operating system can't be found on the optical disc.
	    - To fix this issue, remove the optical disc from the drive and reboot.
	    - There are multiple hard disks in the system, but only one has an operating system installed.
	    - If the boot device setting is inadvertently changed in the BIOS/UEFI, the device will try to boot the system from the wrong hard disk.
	- The master boot record (MBR) has been overwritten or is corrupt.
	    - The MBR is the first sector of the hard drive that tells the BIOS where to look for the operating system on the disk.
	    - If the MBR is damaged or corrupt, the operating system will fail to load.
	    - To fix this problem in Windows, you have to boot from the installation disc to enter the recovery environment and select the Automatic repair option.
	    - Alternatively, you can select the Command prompt option and run the bootrec command to rebuild the boot configuration data. You can also run the bootrec command with the following switches:
	        - /fixmbr—repairs the master boot record.
	        - /fixboot—repairs the boot sector.
	        - /rebuildbcd—rebuilds the boot configuration data.

##### Driver not recognized by the BIOS/UEFI (SAME FOR SSD)
A modern BIOS/UEFI automatically detects drives and their geometry during POST. In older systems, you had to manually enter the disk geometry and it was very common for a wrong value to be entered. In modern systems, this rarely happens. If the BIOS can't detect the drive, it's usually caused by one of the following.

-   The power connector is unplugged.
-   The SATA cable is unplugged.
-   The drive is malfunctioning.

##### Application Crash
If an application you are using crashes, an error has occurred that gives you no choice except to exit the application. Be aware:

-   Sometimes you can fix the problem by rebooting the computer.
-   You may need to debug the system.
-   You can check log files for errors that provide clues about what might have caused the crash.

##### Crash Screens
If you experience a black screen of death (BSOD) on a Windows machine or spinning pinwheel of death (SPOD) on a MAC, several events may have occurred. You could have a fatal system error that is preventing the system from operating safely, or just one application may have failed.

Often, rebooting the computer solves the problem. If that doesn't work, you can:
- Attempt to revert the system to a previous state to undo any software or hardware changes that are causing problems.
- Scan the computer for viruses.
- Roll back drivers, update drivers, update the operating system, update BIOS, or return suspect components to the factory settings.
- Repair permissions.
- Clear the dyld cache on a Mac.

##### Drive Noise
- Excessive or unusual drive noise (such as a clicking or grinding) almost always indicates a failing hard disk. For example, a clicking noise coming from the drive usually indicates one or more failing heads.

##### Data loss or corruption (SAME FOR SSD)
- Corrupt or lost data on the storage device can indicate the disk or one of its components is failing.

##### I/O operations per second (IOPS)
- IOPS is the measurement of how many input/output operation can be performed per second.
	- A decreasing IOPS value (fewer input/output operations are occurring) can indicate that a disk or one of its components is failing.
	- In Windows, IOPS can be measured using the Performance Monitor app.

#### SSD
##### Slow Performance
- The more an SSD is used, the slower the read/write speed will be.
	- Make sure the file system is optimized for an SSD. Because SSDs store data differently than HDDs, they require special techniques (such as wear leveling support) to extend the life of the drive.
	- Update the SSD's firmware. Newer firmware versions fix bugs and optimize how the SSD stores data.
	- Run a manufacturer-specific SSD software utility. Most SSD manufacturers have specialized utilities that can check for errors and optimize an SSD's performance.
	- Check the speed of the SATA connection. Older SATA versions have slower transfer speeds than newer SATA versions. If performance is too slow, consider upgrading components to the latest SATA version.
	- When the SSD is too full, performance decreases significantly. If this happens, try enabling features such as TRIM support in the operating system (OS).

While features such as TRIM help to an extent, the best way to maintain high performance is keeping an SSD below 90% capacity.

### RAID Troubleshooting
When a workstation's hard disk storage is using RAID, you may be required to troubleshoot RAID issues. The following table gives possible causes and fixes for two common issues.

#### The OS cannot find the RAID array
With hardware RAID arrays, this can be caused by:
- A missing device driver for the RAID controller board. To fix, download and install the latest driver for the RAID board.
- A failed RAID controller board. To fix, install a new RAID controller board, rebuild the array, and then restore the data from backup.

With software RAID arrays it can be caused by a serious issue with either the operating system files or with the storage devices included in the array.

#### RAID stops working, but had appropriate drivers loaded
If you have the appropriate driver and RAID stops working, possible issues are:

- The RAID controller board may have failed. To fix, install a new RAID controller board, rebuild the array, and then restore the data from backup.
- One or more drives in the array have failed.
    - In a RAID 0 configuration, the data is striped across all the drives in the array.
        - The loss of a disk means all its data stripes are lost.
        - To fix, replace the failed disk, rebuild the array, and then restore data from backup.
    - RAID levels that include redundancy (such RAID 1, RAID 5, RAID 1+0, and RAID 0+1) can tolerate disk failures better than other RAID levels. Usually, you can:
        - Replace the failed disk.
        - Wait for the data to be automatically restored from the other disks in the array using mirroring or parity

## 5.9.4 SSD Maintenance Facts
### SSD Maintenance
Implementing a solid-state drive (SSD) storage device in a desktop or notebook computer can significantly increase the system's overall performance. However, the same flash memory technology that makes SSDs so much faster than standard hard disk drives also introduces maintenance and troubleshooting issues. The following table lists a few of those issues.

#### Defragmentation
On an SSD storage device, fragmentation is much less of an issue than for standard hard disk drives. File systems such as NTFS still fragment files when writing them to the drive in order to optimize storage space. However, an SSD storage device doesn't have read-write heads, so no repositioning must occur to read heavily fragmented files. As a result, fragmented files can be read as quickly as contiguous files.  
  
When working with SSD drives, do not defragment them as you do standard hard disk drives. SSDs wear out over time. Each cell in a flash memory bank has a finite lifetime and can be written to and erased only a certain number of times before it fails. Running defragmentation utilities causes unnecessary write/erase operations to occur.  
  
To disable defragmentation:
1.  Open the Settings app.
2.  In the **Find a setting** field, type 'Defragment' and then select the **Defragment and optimize your drives** option. This opens the Optimize Drives app.
3.  Under Scheduled optimization, select **Change settings**, clear the **Run on a schedule** option, and select **OK**.

#### Mean time before failure (MTBF)
An SSD storage device has a lifespan called the mean time before failure, which is usually much shorter than standard hard disk drives. Each time a write/erase operation occurs, it consumes some of the finite lifetime of the flash memory chips within the SSD device.

- Some applications running on the system can overuse SSD storage devices. For example, audio, graphic, and especially video editing applications commonly require a large number of write/erase operations and can cause SSD storage devices to fail prematurely.
- However, these applications also benefit greatly from the increased speed offered by SSD storage devices.
- Therefore, if you chose to use SSDs with these types of applications, you should consider configuring an automatic data backup process (such as Windows Backup and Restore or File History) to protect the data stored on the SSD drive on a traditional hard disk drive.

Some system builders implement a mix of storage devices in high performance systems so that:
- Heavily used information is stored on a standard hard disk drive. For example, the Windows operating system and its applications may be installed on a less expensive but more durable standard hard disk drive.
- Only data that requires high performance is stored on SSD storage devices.
- Important data on the SSD is automatically backed up on the standard hard disk drive.

#### TRIM
One method for extending an SSD device's life is to enable TRIM functionality. TRIM configures the operating system to communicate with an SSD device and to tell it the blocks of data on the device that are no longer required and can be wiped clean. This prevents the SSD device from storing unnecessary data and being overused.  
  
Later versions of Windows should automatically detect the presence of an SSD device and enable TRIM. You can verify this by opening Windows Terminal and entering 'fsutil behavior query DisableDeleteNotify'.
- This command will return either a 0 or a 1. A value of 0 indicates that TRIM is enabled, but a value of 1 indicates that it is not. If it is disabled, you can manually enable TRIM on an SSD drive by entering 'fsutil behavior set DisableDeleteNotify 0'.