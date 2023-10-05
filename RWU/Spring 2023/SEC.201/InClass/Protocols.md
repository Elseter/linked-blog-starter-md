
---
aliases: [ "20230202165626",  ]
tags: SEC.201, SEC
date_created: 2023-02-02 16:56
---
[[SEC.201 Index]]
# Protocols
---
## Announcements
- February 15th, no in person classes
	- Doug is on a trip

### General Info
- PKA files have been added to all the assignments so in the future assignments
	- Please submit your PKA in the future
- Assignments close out when Doug grades them, so there is only undetermined period for late work
- Brain dump sites are very, very dangerous
	- There are lots of RATS (Remote access tech) and other malware 
	- do NOT give anyone any money
	- Freeccnaworkbook - if you are looking for a nice site that is actually free

- `warez` sites
	- sites were people put up cracked copies of things
	- Often filled with malware

### Ports
- 65536 possible ports on windows Intel machines
	- FFFFh in hex
- 80/tcp is the standard operating port for web-servers

### OSI Model
![[OSI Model.png]]

### Sniffing and Other Tools
- Sniffing refers to capturing packets off of a network
	- snarfing, snatching packets off the airwaves
- isn't illegal if you own the network
- wireshark
	- program
	- packet sniffing tool
	- turns the nic on your device and it will grab everything it can grab
	- can get you fired
	- can get you kicked out of school
- Hubs
	- Layer 1 devices from days long past
	- plug into the network
	- split out every signal coming to a switch and capture every piece of traffic
- Dsniff
	- Listends on port 23/tcp
	- telnet
	- sends everything in plain ascii text
	- can be set to listen for certain specific phrases
		- such as username and password

## CFAA
- The computer fraud and abuse act was passed in the US in 1986 and amended in 2008
	- 18 USC Section 1030 of Federal Law
	- Many states have additional laws, some very wacky
	- inspired by a movie called Wargames

- The law is vague and basically says that "intentionally accessing a computer without authorization or in excess of authorization" can have penalties
	- It neglects to define a "computer" or "authorization"
	- VERY VERY SCARILY VAGUE
	- Federal Law

- Sentencing
	- 1 to 5 years for basic violation
	- 1 - 10 by causing intentional damage (damage is undefined)
	- and more.