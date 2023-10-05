
---
aliases: [ "20221223125852",  ]
tags: C++, Programming
date_created: 2022-12-23 12:58
---
[[C++ Index]]
# Introduction to C++
---

## How does C++ Work
- C++ is a compiled language 
>[! note] A Compiled Language 
>For a program to run, it's source code must be processed by a **==Compiler==**, producing object files (similar to java class files), which are then combined by a **==Linker==** which results in an ==**executable program**==
- A C++ program typically consists of many source code files 
- The compiled executable is created for the specific hardware/system combination and is NOT portable 
	- You can not compile on Windows and expect the .exe to run on Android
![[C++ Compile Example.png]]

### The ISO C++
- The ISO (aka the International Organization for Standardization) version of C++ is the recognized official standard
- Defines two kinds of entities
	1. **Core Language Features** 
			These are built in types (such as *char* and *int*) and loops (*for*-statements and *while* statements)
	2. Standard-library components
			These are containers (such as *vector* and *map*) and I/O operations ( *<<* and *getline()* )

#### The Standard Library
- The Standard Library components are normal pieces of C++ code that are provided with every C++ implementation
	- It can be implemented in C++ itself, with very minor uses of machine code for things such as thread switching 
>[! warning] Statically Typed
>C++ is a statically typed language. The type of every entity must be known to the compiler at its point of use. The type of the object determines the set of operations applicable to it and its layout within memory

