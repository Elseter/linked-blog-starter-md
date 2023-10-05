
---
aliases: [ "20230905153415",  ]
tags: SEC, SEC.409
date_created: 2023-09-05 15:34
---
# History of Unix
---
## History of Unix
- ATNT, Bell labs 
- several other small unix 
- First linux, 1987
	- Minux
- Linus Torvauld 1991
	- University of Helsinky

- linux is under the gnu heading
	- open source code is available

### Kernels
- Every operating system has a kernel
	- a kernel is the source code at ring 0
		- There are 4 rings
	- The kernel acts as an interface between the hardware and the higher rings
		- ring 1 is drivers
		- ring 2 higher level drivers
	![[Rings.gif]]
	- Linux is a monolithic kernel
	- Modular mods

#### UEFI
- UEFI is the firmware on the motherboard provided by the manufacturer
- It loads the kernel in order as the systems starts to boot up
- UEFI will check to make sure hardware is functioning as it should
- Some firmware drivers are loaded on chips on the motherboard
- Motherboard voltages
	- 3.3 volts
	- 5 volts
	- 12 volts

## Linux
- linux is a non GUI based operating
	- There is no built in native graphical interface
	- A lot of distros will have preinstalled GUIs, but they are not guaranteed
- Major branches
	- Debian
	- Arch Linux
	- Red Hat
	- Gintoo
### Commands
- `apt`
	- `sudo apt get update`
	- `sudo apt get upgrade`
- // build from sources
- `sudo`
	- sudo says make me like root
	- Similar to run as admin on windows
- `sudo passwd`
	- Sets your current user password
- `sudo passwd root`
	- Sets your root password
- `sudo su` {username}
	- Switches you to any other user on the system
- `ls`
	- lists the contents of the current directory
	- `ls -al`
		- Gives you everything
		- Dates, times, sizes, blocks
- `man ls`
	- man is a command that provides a text explanation of a linux command
- `pwd`
	- Where am i?
	- Shows you the current directory listing that you are in
- `who`
	- Who am I?
- `mkdir`
	- Makes a directory at the current location
- `cd`
	- Change to this directory
- `exit`
	- leave
	- In linux, everything is considered a shell
	- exit lets you leave the shell you are in
- `echo "hello" >> foo.txt
	- Appends the text above to the end of the designated file
- Text Editors
	- `nano`
	- `emacs`
	- `Vim`
		- `vim X.+X+`
		- `<inset key>` enter insert mode
		- `<esk>` exit insert mode
		- `:w` save
		- `:w-foo.txt` save as
		- `:q` - quit
		- `:q!` - quit without saving
		- `dd` - delete this line
		- `yy` - copy the text
		- `p` - paste
- `cp`
	- Copy
- `rm`
	- Remove
- `mv`
	- Rename
### File System
- root
	- Root is the base of the filesystem
	- Gaining access to root requires the root password
