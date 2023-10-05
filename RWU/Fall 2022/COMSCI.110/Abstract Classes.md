
---
aliases: [ "20221207110313",  ]
tags: RWU, COMSC.110, COMSC, Programming
date_created: 2022-12-07 11:03
---
[[COMSC.110 INDEX]]
# Abstract Classes
---
## Relevant Links 
[[Objects and Classes]]

## Abstract Classes and Methods
>[! Definition ] Abstract Methods
>- Have header only
>- No body implementation 
>- Intention of wanting to do something, but isn't actually computed as body is empty
>	- The implementation occurs *within a child class*
>- An abstract method CAN NOT be contained in a non-abstract class
>	- A child class must implement all the abstract methods or else it becomes an abstract class itself

>[! definition ] Abstract Class
>- A class that contains abstract methods

### Object Creation
- You CAN NOT create an object from an abstract class
	- you can still define its constructors
	- These constructors will then be implemented in non-abstract children classes

### Classes
- A class that contains abstract methods must be abstract
- However, it is possible to define an abstract class with no abstract methods