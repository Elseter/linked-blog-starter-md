
---
aliases: [ "20230328140511",  ]
tags: SEC.340, SEC
date_created: 2023-03-28 14:05
---
[[SEC.340 Index]]
# Mechanization of Secrecy
---
## Background
- Mixed blessings of radio
	- End of the 19th century
	- Ease of communication
	- Ease of interception

- Advent of the Great War
- The need for effective encryption - intensified

### German ADFGVX cipher
- one of the most famous wartime ciphers
- Introduced on March 5th of 1918
- Cipher's strength lay in its convoluted nature
	- It is a mixture of substitution and transposition

**Step 1**
- Draw up a 6 * 6 grid
	- Fill the grid with random arrangement of the 26 letters and 10 digits
	- Key - arrangement

**Step 2**
- Take each letter of the message
- Locate its position in the grid
- Substitute it with the letters that label its row and column
	- Monoalphabetic substitustion 

**Step 3**
- Pick a keyword: e.g. MARK
- Write the letters of the key word in the top row of a fresh grid
- Rearrange the columns of the grid in alphabetic order
- Going down each column and write out the letters in new order

### ADFGVX cipher
- Cracked quickly
- Cryptanalysis can affect the course of the war at the very highest level
	- Breaking Zimmermann's telegram

- Codebreakers had maintained the upper hand over codemakers

## One Time Pad Cipher
- As the great war drew to a close
- Major Joseph Mauborgene - head of cryptographic research for the US Army
- Introduced the idea of a Random Key - no meaningful words
- Keys were shared by sender and receiver
- Keys are destroyed once the message has been sent, received and deciphered 
- Thus the name- One Time Pad Cipher

### One Time Pad Cipher
- Security due to the randomness of the key
- No patterns, no structures, nothing the cryptanalyst can latch onto
- Not merely believed to be unbreakable (as Vigenere Cipher)
- Can mathematically proved to be unbreakable
- Offers guarantee of security - **Holy Grail of Cryptography**

- In theory - the perfect cipher
- In practice - difficult
	- There is the practical problem of making large quantities of random keys 
	- Difficulty of distributing random keys

### Cipher Machines
- Cipher Disk (Cipher Wheel)
![[Pasted image 20230328142053.png]]

#### Enigma
- German inventor Arthur Scherbius
- Developed a piece of cryptographic machinery - **Enigma**
- Three major parts
	- Keyboard
	- Scrambler
	- Lampboard

