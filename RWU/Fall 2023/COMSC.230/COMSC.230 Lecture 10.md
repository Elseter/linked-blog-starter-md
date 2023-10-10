---
aliases:
  - "20231009160328"
tags:
  - COMSC
  - COMSC230
date_created: 2023-10-09 16:03
Index: "[[COMSC.230 Index]]"
---
# COMSC.230 Lecture 10
---
## Lecture Topics
- Create, read, write and update files
- Perform sequential file processing
- Understand the differences between formatted-data and raw data file processing
### Into to file processing
- Variables, lists, tuples, dictionaries, sets, arrays, pandas series and panda DataFrames offer only temp data storage
- lost when a local variable "goes out of scope" or when the program terminates
- Data maintains in files is persistent
- Computers store files in secondary storage devices solid state drives, hard disks, and mote
#### Standard File Objects
- When a python program begins executing
- 3 file object datatypes
#### Writing to a text file: introducing the with statement
- Many applications acquire resources
	- files, network connections, database connections, and mote
- Should release resources as soon as they're no longer needed
- Ensures that other applications can use the resources
- `with` statement
	- Aquire a resources and assigns it corresponding value
##### Reading data from a .txt file
- 