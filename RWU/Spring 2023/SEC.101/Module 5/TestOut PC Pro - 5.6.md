
---
aliases: [ "20230217135444",  ]
tags: SEC.101, SEC, PCPro
date_created: 2023-02-17 13:54
---
[[SEC.101 Index]]
# TestOut PC Pro - 5.6
---
## 5.6.4 Storage Management Facts
- To add space to existing volumes use one of the following strategies

### Configure a Mount Point
- A mount point is an empty folder on the existing volume that points to another partition. Data saved to the folder is physically saved on the referenced partition. Key points are:

	- The volume with the empty folder must be formatted with NTFS.
	- You can create mount points on basic or dynamic volumes.
	- The folder on the source volume must be empty.
	- The target partition must not have a drive letter.

Using a mount point is the only way to add space to the system volume using space on a different disk or non-contiguous disk space.

### Extend the Volume
- When you extend a volume, you add unallocated disk space to the volume.

- For basic volumes, you can extend the volume only onto the same drive using contiguous unallocated space. Many third-party partitioning tools can extend partitions regardless of the operating system.
- To extend the volume onto the same drive using non-contiguous unallocated space or to extend the volume onto another disk, convert the disk to a dynamic disk and extend the volume.
    - An extended volume uses disk space on the same disk.
    - A spanned volume uses disk space on a different disk.

- You can extend a system volume only by using contiguous free space on the same disk. This is the same for both basic and dynamic disks.
- Volumes must be unformatted or formatted with NTFS to be extended.