
---
aliases: [ "20221114110943",  ]
tags: RWU, COMSC.110, COMSC, Programming
date_created: 2022-11-14 11:09
---
[[COMSC.110 INDEX]]
# Polymorphism
---
# Polymorphism
## Introduction
- an object oriented concept that allows us to create versatile software designs
- _Polymorphism_ means "having many forms"
- A _Polymorphic Reference_ is a variable that can refer to different types of objects at different points in time
	- methods invoked through PR can change from one invocation to the next
```java
Holiday day = new Holiday();
// time passes
day = new Christmas();
// where christmas is a child class of holiday
```
![[COMSC.110 polyimg.png]]

### Subtype and Supertype
>[!definition] Definition
>A class defines a type. A type defined by a subclass is called a **Subtype**

>[!note] Definition
>A class defines a type. A type defined by its superclass is called a **Supertype**
- Circle is a subtype of GeometricObject and GeometricObject is a supertype for Circle

### Dynamic Binding

### Casting from Superclass to Subclass
```java
Apple x = (Apple)fruit;
Orange x = (Orange)fruit;
```
- Requires explicit declaration (casting)

### Protected Modifiers
| Modifier  | Scope                                           |
| --------- | ----------------------------------------------- |
| public    | can be accessed by everyone                     |
| private   | can be accessed in the same class               |
| default   | can be accessed by anything in the same package |
| protected | can be accessed by the same family (inheritance) or same package                                                |
