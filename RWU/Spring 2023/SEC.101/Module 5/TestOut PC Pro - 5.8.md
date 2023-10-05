
---
aliases: [ "20230219162526",  ]
tags: SEC.101, SEC, PCPro
date_created: 2023-02-19 16:25
---
[[SEC.101 Index]]
# TestOut PC Pro - 5.8
---
## Disk Optimization 5.8.5
- This lesson covers the following topics
	- Disk Drive Upgrade
	- Disk Cleanup

### Disk Drive Upgrade
Optimizing a hard disk drive can improve a computer's overall performance.

#### Upgrading the Hard Disk
- Upgrade to the fastest disk possible. Disk drives come in a variety of rotation speeds such as:
	- 5400 RPM (not desired)
	- 7200 RPM (minimum)
	- 10,000 RPM
	- 15,000 RPM
- Some hard drives do not use rotating disks such as:
	- Solid-state drives
	- NVMe (nonvolatile memory express) solid-state drive
	- NVMe M.2 (nonvolatile memory express) solid-state drive

#### Upgrade the Disk Interface
- Upgrading a disk interface significantly improves the throughput of data to and from a disk drive. For optimal performance, consider upgrading to PCIe. This will upgrade the speed to 4,000 Mbps.

### Disk Clean-up
- A mostly full drive can run slower than a mostly empty one.

#### Disk Cleanup App
- The Disk Cleanup app helps manage disks by locating and disposing of files that can be safely removed from the disk. It:
	- Empties the Recycle Bin.
	- Deletes temporary files such as those used by a web browser or for application installation.
	- Deletes installation log files.
	- Deletes offline files.
	- Compresses old files.
- To run Disk Cleanup, type 'disk cleanup' in the Windows search box. Then select the Disk Cleanup app from the Best match list.

#### Optimize Drives App
The Optimize Drives app optimizes the performance of a hard drive by joining fragments of files that are in different locations on the hard drive.

- To improve defragmentation, disable programs such as screensavers and virus software that run in the background. Any disk access (whether reading from or writing to the disk) while Disk Defragmenter is running slows down the defragmentation process.
- The more information that is on the drive, the more time it will take to defragment the drive.

- It is important to not defragment or optimize a solid-state drive (SSD). Although files can become fragmented on an SSD, it is not important to defragment them because the seek time is about 0.1ms.  
  
- To run Optimize Drives, type 'Defrag' in the Windows search box. Select the Defragment and Optimize Drives app from the Best match list. You can also run this app as follows:
	1. Open File Explorer and select This PC.
	2. Right-click the drive you want to defragment and select **Properties**.
	3. From the Tools tab, under Optimize and defragment drive, select Optimize.

#### Check Disk (Chkdsk)
Check Disk (chkdsk) is a utility that verifies the file system integrity of a hard disk. Errors that can be checked and fixed by Check Disk include:

- Lost clusters. These are a series of used clusters on the hard disk drive that are not associated with a specific file.
- Cross-linked files. This occurs when two files claim the same cluster. Check Disk identifies cross-linked files and corrects the cluster associations.
- Orphaned files. These are files that exist on the hard drive but are not associated with a directory in the index. Normally Check Disk can re-associate the file with the correct directory.
- A bad sector. This is a portion of the hard disk that cannot be used. Bad sectors are marked so the system doesn't try to use them. Any used bad sectors are redirected to another sector.

You can run chkdsk by opening a Windows terminal and typing 'Chkdsk' at the PowerShell prompt.
	- Use Chkdsk with the /f switch to automatically fix errors without scanning for bad sectors.
	- Use the /r switch to scan and fix bad sectors and other errors.
	- Use the /? command for help.