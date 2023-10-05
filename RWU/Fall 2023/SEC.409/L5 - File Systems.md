---
aliases: [ "20231003153256",  ]
tags: SEC, SEC409
date_created: 2023-10-03 15:32
---
# L5 - File Systems
---
## File Systems
- Every OS has to have a file system to manage the storage of files on various devices rather than memory
- This is basically just the mechanism which allows you attach storage and write/read to and from it
- In Windows this is called **NTFS** or older versions called it **FAT** (those are both different systems that were used by Microsoft)
- Linux has used various file systems and most often uses **EXT4** currently but it can support many others. In fact you can mount many different pieces of media with different file systems and look at them in linux
- This was/is a common tactic to get around security. If security is OS based, it may not work in a different OS
### Old Fashioned Example
- Microsoft used to write the passwords to the disk in plain text but if you tried to look at it in windows, it fails
- Since you know where you want to look, you can mount the drive in a linux machine and there it is
	- This no longer works
### Components
- On top of the physical file system there is a virtual file system
- Naming Convention
- Directory Management
- File Metadata
- file management tool in the API
#### Things file systems have
- **Space management**
	- How do we allocate the space on this device with considerations of the physical storage
		- Understand that files will be written to available space and deleted files are marked for deletion
		- This creates some issues from a coding perspective. Basically if I write 6 files that are each 2 bytes and then I delete one of the 2 byte files in the middle. The next time I try to write a 4 byte file, 2 bytes will go into the empty space and 2 bytes will be tacked to the end
		- Linked list concepts are used to locate all the pieces
		- So, the file system maintains a link to the physical location of the start of the file and each chunk has a pointer to the next chunk
		- If this gets out of hand, it is called fragmentation and "defragging" the drive may be necessary to improve performance
##### In Linux
- Files have names, metadata, directory structures, and so forth
- Each file has an inode entry that contains the size, permissions, ownership, and location of the file and its directory
- Ext was introduced in 1993. It is a non journaling
###### Ext4
- Can support large file systems
- Maximum file name is 255 bytes
- Largest file is 16TB
- Maximum number of files $2^{32}$ 
- Has some journaling checksums which can allow identification of bad files after a crash
>[! summary]  Configuring
>You can use whatever linux will allow (which is most everything)
>- I would research carefully
#### Actions
- Mounting and Unmounting drives
	- `mount <options>` device directory
		- `sudo mount -o ro /dev/sda3/myDirectory`
	- This would mount a partition called SDA3 and you would see the contents in /myDirectory
	- It is a good idea to mount as read only just in case
	- `-t` as an option will mount a specific file system type
	- `sudo umount /myDirectory` - Unmount the whole thing
		- `sudo umount -f /myDirectory` - will force it so if someone is using the files, they can be damages
##### /etc/fstab
- In modern versions of linux, there is a lot of automation, but old versions of linux used to be manually done
- This file is a listing of partitions on the system that can be used by mount
- Do not mess with this on systems you value
>[! note] blkid
>`blkid` can be used to display the UUID of the partitions
##### fsck
- very dangerous tool in some ways, but in a way to try and recover damaged partitions
	- practice practice practice with this tool before using it on a live system
	- VERY DANGEROUS
#### Adding Drives
- This is a lot easier since most modern linux kernels support adding SATA type hardware just by plugging it in
- Sata disks usually are named sda, sdb, etc...
##### Fdisk and parted
- This is the management tool that you use to create partitions, delete partitions
#### Mkfs
- Command to create a file system in a partition
	- `sudo mkfs.xfs /dev/ubuntu/var`
	- The /dev/Ubuntu/var is the mount point for this xfs file system
## Raid 
- RAID is a very useful server tool and different RAID levels are used to manage drive collections
	- **RAID 0** - striping across at least two drives (not a backup)
	- **RAID 1** - mirroring across at least two drives (not a backup)
	- **RAID 5** - striping across three drives, any one drive can fail and be rebuilt from the other two
	- **RAID 6** - striping across three drives, any two drives can fail and be rebuilt from the other two