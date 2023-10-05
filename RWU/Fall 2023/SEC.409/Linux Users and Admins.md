
---
aliases: [ "20230912154149",  ]
tags: SEC, SEC.409
date_created: 2023-09-12 15:41
---
# Linux Users and Admins
---
### Users
#### useradd
- `useradd <uname>`
- `useradd -m <uname>`
	- creates a home directory for the user
	- They have write and read privileges for just that directory
	- /home/\<uname>
- `useradd -g` - default group
	- This create a user and adds them to the default group
- `useradd -g gname`
- `useradd -s` - default shell
	- In ubuntu/debian, the default shell is bash
- `useradd -s /usr/bin/csh`
	- This adds a user with csh set as the default shell
- `useradd -e` 2023-12-31
	- This will add an expiration date for an account

#### usermod
- `usermod -aG` 
	- append a group

>[! example]
>```bash
>usermod -aG sudo foo, bar, e170

- `useradd -G sudo dwhite`
	- This will add a user called dwhite who will be added to the sudo group
	- This will add dwhite to the sudoers file which allows that user to run sudo commands

#### userdel
- deletes a user

#### passwd
- How to change passwords
- with no following qualifiers, it will change the current user password
- `password <otherUser>`
	- allows you to change other users passwords if you have permission

>[! bug] Where Passwords
>**/etc/shadow** and **/etc/passwd** have the usernames and the links to the hashes to the passwords hidden on the disk

#### man
- the man page is the manual page for every linux command

### File Names
- case sensitive
	- needs exact spelling to be accurate
- No extensions
	- in BASH we tend to use .sh
	- in AWK we tend to use .awk

### Symbolic Links
- uses the command `ln -s`
	- `ln -s /usr/bin/ls dir`
		- Creates a symbolic link between ls and dir
	- `ls -s /etc/shadow foo`

### Block Devices
- Refers to storage
	- Hard Drive, Flash Drive
	- Found in /dev/
		- `ls /dev/`
			- Lists all partitions and drives
		- `ls -l`
			- lists block devices (b)

## Permissions
- `ls -al /etc/shadow`
	- This will return all files and directories in shadow
	- Each item will be proceeded by 10 values
	- _ {_ _ _ } { _ _ _ } {_ _ _ }
		- 1-3 are r w x for owner
		- 4-6 are r w x for group
		- 7-9 are r w x for others 

#### chmod
- This command allows us to change the permissions on files and directories
- `chmod 4, 2, 1`
	- 4 is read
	- 2 is write
	- 1 is execute
		- Add the values that you want permissions for 
- `chmod 777 /home/dwhite/foo.sh`
- `chmod 777 *`
- `chmod` commands also work with letters
	- `chmod u+rwx` - gives users r w and x
	- `chmod g+r` - gives groups read
	- `chmod u-x` - takes away users ability to run a file
	- `chmod a+x` - gives other ability to run

#### chown
- Take ownership of a file
- Give away ownership of a file
#### chgrp
- Change the group ownership of a file
#### gzip and tarballs
- gzip is a compression tool
- gunzip is an expansion tool
- tar stands for tape archive
- Now tar is a directory tree
- `tar -a /home/dwhite/* backup.foo`
	- This would take all the files in home/dwhite and place them into backup.foo
	- These are not compressed by default
	- `gzip backup.foo.tar`
		- creates `backup.foo.tar.gz`
- `tar -zxvf <filename>`
	- Extract a tarball

#### which
- weird and old command
- looks for things on the $PATH
- `echo $PATH`
	- Will show you your path

#### find
- works in the same way as which
	- Only it works on the ENTIRE hard drive
	- Takes a very very long time
