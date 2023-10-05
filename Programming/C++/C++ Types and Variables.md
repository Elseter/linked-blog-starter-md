
---
aliases: [ "20221224225154",  ]
tags: C++, Programming
date_created: 2022-12-24 22:51
---
[[C++ Index]]
# C++ Types and Variables
---
## Types
- every name and every expression has a type that determine the operations that can be preformed on it
>[! example] Type Example
>```cpp
>int inch;
>```
	- This specifies that inch is of the type int, inch is an integer variable
- A **Declaration** is a statement that introduces an entity into the program and specifies its type
	- A **Type** defines the set of possible values and set of possible operations (for an object)
	- An **Object** is some memory that holds a value of some type.
	- A **Value** is a set of bits interpreted according to a type
	- A **Variable** is a named object

- Each fundamental type corresponds directly to hardware facilities and has a fixed size that determines the range of values that can be stored in it:
![[C++ Type Sizes.png]]

- A char is of the natural size to hold a character on a given machine (typically an 8-bit byte)
	- The sizes of other types are typically ==**multiples of char**==
- Numbers can either be floating point, which contain a decimal or exponent, or integer by default decimal
