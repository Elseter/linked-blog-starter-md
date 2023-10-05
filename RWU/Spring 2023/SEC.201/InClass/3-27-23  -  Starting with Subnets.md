
---
aliases: [ "20230327165756",  ]
tags: SEC.201, SEC
date_created: 2023-03-27 16:57
---
[[SEC.201 Index]]
# Starting with Subnets
---
- Subnetting has been haunting networking majors for the past several centuries
## Understanding Subnetting
- The ones in the subnet mask represent network portions
- The zeros in the subnet mask represent host portions
- That's the whole thing

>[! tip] Most common
>255.255.255.0 
>- also represented by /24
>- CIDR
>- 24 bits that are on, starting from the left

### So, let's do a bit more
- Consider classful networking
	- 0.0.0.0 - 127.255.255.255 is called a class A (0000 0000 - 0111 1111)
	- 128.0.0.0 - 191.255.255.255 is called class B (1000 0000 - 1011 1111)
	- 192.0.0.0 - 223.255.255.255 is called class C (1100 0000 - 1101 1111)

- Please remember RFC 1918 address in these classes
	- 10.0.0.0 /8 == Class A Private Address
	- 172.16.0.0 / 16 == Class B Private Address
	- 192.168.0.0 /24 == Class C Private Address

- These addresses are all used for internal, private networks and cannot be used on the public internet
- When these addresses are seen on public networks, they are called bogons

### The Subnet
- Fixed length subnets are typically 
	- /8 or the first 8 bits
	- /16 
	- /24

- So, if we use 10.1.1.0/24
	- That means 
		- 0000 1010.0000 0001.0000 0001.0000 0000
	- With the mask
		- 1111 1111.1111 1111.1111 1111.0000 0000

- That means that 10.1.1 is the network portion