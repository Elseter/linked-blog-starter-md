
---
aliases: [ "20230126114844",  ]
tags: COMSC.111
date_created: 2023-01-26 11:48
---
[[COMSC.111 Index]]
# B.1-B.4, B.16
---
## B.1 Overview of Object Orientation
### Objects and Classes
>[! tip] Java
>Java is an object oriented language
---
>[! def] Object
>An Object is a fundamental entity in a java program.
>- An object is defined by a class, which can be though of as the data type of the object
>- Once a class has been defined, multiple objects can be created from that class
>- `Encapsulation`, meaning that each object protects and manages its own information
	- The act of invoking a method on an object is sometimes referred to as **sending a message** to the object
### Inheritance
- Classes can be created from other classes using `inheritance`
	- The new class will have the properties of the parent class, as well as newly defined variables and methods that are exclusive to the child class
	- Further classes can then be derived, creating a hierarchy of classes

## B.2 Using Objects
>[! example]
>```java
>System.out.println("Test Print");
>```
- The `System.out` object represents the output device or file
	- The objects name is `out`, and it is stored in the `System` class
	- The `println` method refers to a service that the `System.out` object preforms for us

### Abstraction
- An object is an `abstraction`, which means that the precise details of how it works are irrelevant from the point of view of the user of the object
>[! tip] Human Memory Storage
>Sometimes it is important to hide or ignore certain details. The human mind can, on average, only handle seven pieces of information within short term memory
>- When we group pieces of information together into chunks, these only count as one piece
>- Ex. You don't need top know how to drive a car to use one
>- Initially, all cars had a manual transmission. The driver had to know how to manage and control the gears. However, modern cars are now automatic, and the driver does not need to be aware of how to change gears. Those details were hidden by raising the `level of abstraction`
---
>[! key] Key Details
>An abstraction hides details. A good abstraction hides the right details at the right time so that we can manage complexity

### Creating Objects
- A java variable can either hold a primitive value or a `reference to an object`
```java
name = new String("James Gosling");
```
>[! def] 
>The act of creating an object by using the new operator is called **`instantiation`**
- An object is said to object is said to be an `instance` of a particular class
- Once created with the constructor, we can use the dot operator to access methods

## B.3 Class Libraries and Packages
- A `class library` is a set of classes that supports the development of programs.
	- The String class, for instance, is not an inherent part of the Java language. It is part of the `Java standard class library` that can be found in any Java development environment.
>[! def] API
>The class library is made up of several clusters of related classes, which are sometimes called Java APIs. API stands for **`application programmer interface`**. 
---
>[! def] Packages
>A package is a Java language element used to group related classes under a common name.

### Import Declaration
- The classes from `java.lang` are automatically included in every program
	- However, if we want to use classes from any other package we must either `fully qualify` the reference or use an `import declaration`
>[! def] Fully Qualify
>You could use its fully qualified name, including the package name, every time it was referenced. For example, every time you wanted to refer to the Random class that is defined in the `java.util` package, you could write `java.util.Random`.
---
>[! def] Import Statement
>This declaration asserts that the Random class of the `java.util` package may be used in the program. Once this import declaration is made, it is sufficient to use the simple name Random when referring to that class in the program.
>```java
>import java.util.Random;
>// or
>import java.util.*;
>```
	-Using the second option will import all the classes in `java.util`. This should be done if 2 or more class are being used from that package

## B.4 State and Behavior
- Formally, we say the properties that describe an object, which are called `attributes`, define the object’s `state of being`. Variables = Attributes = State of being
- Activities define the object’s `behavior`. Methods = Behavior

## B.16 Exceptions
- Problems that arise in a Java Program may generate exceptions or errors. 
>[! def] Exceptions
>An `exception` is an object that defines an unusual or erroneous situation.
>- An exception is thrown by a program or the run-time environment, and it can be caught and handled appropriately if desired
---
>[! def] Error
>An `error` is similar to an exception, except that an error typically represents an unrecoverable situation 
>- These should not be caught

- A program can be designed to process an exception in one of three ways:
	1. Not handle the exception at all
	2. Handle the exception where it occurs
	3. Handle the exception at another point in the program

>[! tip] Key Concept
>The messages printed by a thrown exception indicate the nature of the problem and provide a method `call stack trace` which indicate where the exception occurred

### The `try` Statement
>[! def] `try catch` block
>A `try` statement consists of a `try` block followed by one or more `catch` clauses. The `try` block is a group of statements that may throw an exception. A `catch` clause defines how a particular kind of exception is handled.
	- A catch clause is sometimes called an exception handler

>[! example] Example of `try catch`
>```java
>try
>{
>	// statements that may throw error
>}
>catch( IOException exception)
>{
>	// statements that handle IOException
>}
>catch( NumberFormatException exception)
>{
>	// statements that handle the number format problem
>}
>```

### Exception Propagation
>[! tip] Key Concept
>If an exception is not caught and handled where it occurs, it is propagated to the calling method. This is called `propagating the exception`
---
>[! tip] Key Concept
>A programmer must carefully consider how exceptions should be handled, if at all, and at what level.

### The Exception Class Hierarchy

>[! tip] Key Concept
>A new exception is defined by deriving a new class from the `Exception` class or one of its descendants

![[Java Exxception Tree.jpg]]