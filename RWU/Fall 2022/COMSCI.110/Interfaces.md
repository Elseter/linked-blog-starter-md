
---
aliases: [ "20221209110359",  ]
tags: RWU, COMSC.110, COMSC, Programming
date_created: 2022-12-09 11:03
---
[[COMSC.110 INDEX]]
# Interfaces
---
## What is an Interface (Java)
>[! definition] Definition
>An interface is a class-like construct that contains *only* **constants** and **abstract methods**
- [[Objects and Classes]]
- In many ways, an interface is similar to an abstract class, but the intent of an interface is to specify common behaviors for objects 
	- For example, you can specify that objects are comparable, edible, and/or clone-able using interfaces 

### Defining an Interface
```java
public interface InterfaceName{
	constant declarations;
	abstract method signatures;
}
```
