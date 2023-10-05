
---
aliases: [ "20221205110624",  ]
tags: RWU, COMSC.110, COMSC, Programming
date_created: 2022-12-05 11:06
---
[[COMSC.110 INDEX]]
# Exceptions
---
## Exceptions
- Exception handling is an important aspect of object-oriented design
>[! Definition]
>- An *Exception* is an object that describes an unusual or erroneous situation
>- Exceptions are *thrown* by a program, and may be *caught* and *handled* by another part of the program
>- A program can be separated into *normal execution flow* and an *exception execution flow*

### Exception Family Tree
![[COMSC.110 Exception Tree.png]]

### Exception Handling
- If an exception is ignored by the program, the program will terminate abnormally and produce the appropriate error message
	- The message includes a <u>call stack trace</u>
		- which indicates the line on which the exception occurred
		- Shows the method call trail that lead to the attempted execution of the offending line 