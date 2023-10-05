
aliases: [ "20230926153313",  ]
tags: SEC, SEC409
date_created: 2023-09-26 15:33
# L4 - Managing Users
---
## UIDs
- all users have UID which is a PID for users. Groups have GIDS
- Users in linux are either users or superusers
- Some users from /etc/passwd
	- Username
	- x == password placeholder
	- UID
	- GID, can also have a gecos (group name)
	- Directory
	- shell
### That x
- The x is a salted password which means it is encrypted and stored elsewhere
	- /etc/shadow
- This is a dangerous thing to allow anyone to have access. With the passwd and shadow files together you can often crack passwords out of linux
>[! bug] Note
>Protect the shadow file with your life
- Common cracking tool called john the ripper
### User account layouts
- .bashrc and .profile
	- Files that start with a . that are hidden. But they still display with ls -al
	- These are bash config files (as per the assignment we did)
	- These are usually found in the "home" directory for the user 
		- However, they may be elsewhere
### Epoch Time
- Unix and Linux use what is called Epoch time
- This is an arbitrary designation for the beginning of the universe and that date is 1 January 1970 at 00:00:00 UTC
- This is the number of seconds that have passed since that day
- These can be timestamps that look like 1695563529 (this morning)
- The command date +%s will show you the current epoch time stamp
- This is a 32 bit integer. That means that after $2^{31}$-1 seconds
	- This date is 19 January 2038 at 3:14:07 UTC
#### Interlude about Y2K
- Y2K was a similar problem
### User Management
- Useradd - note this is just one of the many possible setup configs with useradd
- `Useradd -e 2023-12-31 -G sudo -m mrfufu`
- Usermon - makes changes to existing users
- Userdel - Delete that user
	- Doesn't delete files and directory
	- `Userdel -rf mrfufu`
		- This will delete their files and home directory
- `Groupadd, groupmod, groupdel`
### Boot ups
- `Dpkg -l | grep -i grub` - this is the command that shows the bootloader version
	- Dpkg is for debian, rpm is the version of redhat
- `MBR` - master boot record - this is the part of the hard drive which has the basic intrsuctions for loading the OS
- The MBR is the first 512 bytes of the drive
- You can have multiple MBRs to cause different effects or to load different OS
- `Dd if=/dev/sda of=/tmp/MBR_COPY bs=512`
#### The Boot Process
- The kernel loading is done by Grub so if you want to use different kernels or custom kernels, you will need to modify the grub config
	- Grub config is in /boot/grub
	- Grub.cfg has the instructions for the loading process
- After the kernel is laoded a process called the init or system (modern) process is run. This is based on a file called /etc/initab which sets what is called the run level for this boot
- There are 7 run levels in linux
	- 0 == poweroff
	- 1 == single user mode
	- 2 == multiuser without networking (safe mode)
	- 3 == normal
	- 5 == x win based login instead of text based (normal for gui based systems)
	- 6 == reboot
- Systemd is found in /usr/lib/system/sysstem (system files) and /etc/system/system/ (admin installed)
### Note about single user mode 
- Consider that single user mode can be used without logging in so this means you can reset the root password if you can get into single user mode
	- As soon as the boot process start - press esc whic hwill kick you into the GRUB boot prompt
	- Press E to edit the kernel you are using
	- In the script windows, you can find the ine which says linux /boo/ and add init=/bin/bash
#### Protecting yourself from this
- So, if you implement some solution (there is a setting in systemd you can use to prevent it from opening)(google this)
	- My concern is that if you block this, well, if you lose the root password, you are done
		- Create a special recovery user who can use sudo. Give this user a very strong password. Keep a physical copy of this password in a very safe place. This gives you a way to change the root password without using root or single user mode
	- But you need physical access to get to single user mode. That means keep your servers locked up and lock the racks. The only people that can even attempt this first have to break into your server room

>[! note] 
>mailx is a command that sends you an email

### Installing a script
- Set the permissions to 755 if you haven't
- Move the script into /usr/local/bin/
- Write a service unit script
- Then move the script into /etc/systemd/system
- restart the systemd daemon
	- sudo systemcl daemon-reload
- The command service is used to run it
### Boot 
- sudo systemctl enable redbull.service
### Shutting down or rebooting
- Ideally you don't do this often, but with VMs it has become a more common thing I guess
	- sudo shutdown -h now
	- sudo shutdown -r now

- IPL
	- Intentional power loss is a term used within mainframes to describe the elaborate shut down processes they required
	- Have a guide on how to power down and power up any server