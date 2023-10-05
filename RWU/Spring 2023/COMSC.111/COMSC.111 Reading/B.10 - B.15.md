
---
aliases: [ "20230201072806",  ]
tags: COMSC.111, COMSC
date_created: 2023-02-01 07:28
---
[[COMSC.111 Index]]
# B.10 - B.15
---
## B.10 The static Modifier
- visibility modifiers enable us to specify the encapsulation characteristics of variables and methods within a class
>[! def] Static Modifier
>The static modifier associates a variable or method with its class rather than with an object or instance of that class. 
>- An object is an instance of a class

### Static Variables
- Instance variables
	- is accessed through a particular instance of a class
	- Each object has distinct memory space for each variable, allocated upon initialization 
- Static variables
	- also known as a class variable
	- is shared among all instance of a class
	- There is only one copy for all instances of a class
```java
private static int count = 0;
```
>[! tip] Key Concept
>A static variable is shared among all instances of a class. Changing it in one instances, changes it for all instances

### Static Methods
- A static method (also called a class method)
	- can be invoked through the use of the class name and the dot modifier
```java
System.out.println(Math.sqrt(27));
```
- The main method is also a static method, to prevent the interpreter from instantiating an object that contains the main
- Static methods can not reference instance variables
- They must only utilize static variables or parameters passed into them at the call
	- static or local variables

>[! tip] Key Concept
>A method is made static by using the static modifier in the method declaration

## B.11 Wrapper Classes
- In java, there are primitive types in addition to classes and objects
	- Having two categories of data to manage (primitive and object references) can be tricky at times
	- Sometimes we may wish to only use classes, but need to store a primitive data type
- Then we use a wrapper class

>[! tip] Key Concept
>A `wrapper class` represents a primitive data value so that it can be treated as an object
>```java
>Integer ageObj = new Integer(45);
>```
- The ageObj object represents the primitive value of the int 45
- For each primitive type, there exists a wrapper class defined in the `Java.lang` package
	- However, the wrapper for void can not be instantiated 
- Additionally, these wrapper classes (such as `Integer` ) contain useful methods

## B.12 Interfaces
- Interfaces means the public methods through which we interact with an object
>[! def] Java Interface
>A java interface is a collection of constants and abstract methods
>- An abstract method is a method that does not have any implementation
>- There is not body of code defined for an abstract method
>- The header of the method is simply followed by a semicolon
>```java
>interface Complexity
>{
>	void setComplexity(int complexity);
>	int getComplexity();
>}
>```

>[! tip] Key Concept
>An interface is a collection of abstract methods. It cannot be instantiated
- An abstract method can be proceeded by the word `abstract`
	- Although in interfaces it is not

- A class implements an interface by providing method implementations for each of the abstract methods defined in the interface
	- It must implement all abstract methods
>[! tip] Key Concept
>A class implements an interface which formally defines a set of methods used to interact with objects of that class

>[! example]
>```java
>class question implements Complexity
>{
>	int difficulty;
>	
>	void setComplexity(int complexity)
>	{
>		this.difficulty = complexity;
>	}
>	int getComplexity()
>	{
>		return difficulty;
>	}
>}
>```
- Multiple classes can implement the same interface
- A class can also implement more than one interface
```java
class ManyThings implements Interface1, Interface2, Interface3
```
- An interface may also contain constants, defined using the `final` modifier
	- When a class implements an interface, it gains access to all the constants within it

### The `Comparable` Interface
- The java standard library contains interfaces as well as classes
	- The `Comparable` Interface is one such, defined in the `java.lang` package
- It contains just one method, `compareTo` which takes an object as a parameter and returns an integer
	- Intends to provide a method to compare objects

## B.13 Inheritance
>[! tip] Key Concept
>Inheritance is the process of deriving a new class from an existing one

### Derived Classes
- The new class automatically contains some or all of the variables and methods from the the original class
	- Then the programmer can add new variables and methods to the new class or modify existing one
>[! tip] Key Concept
>Our purpose in using inheritance is to reuse existing software
>- Inherited variables and methods can be used in the derived class as if they had been defined locally
>- Inheritance creates an is-a relationship between all parent and child classes

- The original class, used to derive a new one is called the `parent class`, `superclass`, or `base class`
	- The derived class is called the `child class` or the `subclass`
	- Java uses the word `extends`

>[! bug] Remember
>All horses are mammals, but not all mammals are horses. All subclass will have the material of their superclasses, but superclass will not have the material of their subclasses

```java
class Dictionary extends Book
```
### The `protected` modifier
- Not all variables are inherited in a derivation
- **==The child class inherits variables and methods that are declared public, and does not inherit those that are declared private==**
	- So this creates a need for another visibility modifier, `protected`
		- `protected` methods and variables can be accessed by any class in the same package
>[! tip] Key Concept
>Visibility modifiers determine which variables and methods are inherited. Protected visibility provides the best possible encapsulation that permits inheritance
- Constructors are not inherited in a derived class
	- Constructors are specific to each type of object and object name

### The `super` Reference
- The reserved word `super` can be used in a class to refer to its parent class
	- Used like the `this` reference
	- One use of the super constructor is to invoke the parent's constructor
```java
super(x, y, z);
```
- A child's constructor is responsible for calling its parents constructor
	- Generally, the first line of a constructor should use the `super` reference to call the constructor of the parent class 
	- If not exists, java will automatically call it

>[! tip] Key Concept
>A parent's constructor can be invoked using the `super` reference
- The `super` reference can also be used to reference other variables and methods defined in the parent's class

### Overriding Methods
- When a child class defines a method with the same name and signature as a method in the parent, we say that the child’s version overrides the parent’s version in favor of its own.
- A child class cannot override a method defined with the `final` modifier
>[! tip] Key Concept
>A child class can override (redefine) the parent's definition of an inherited method

## B.14 Class Hierarchies
>[!tip] Key Concept
>The child of one class can be the parent of one or more other classes, creating a class hierarchy
- These hierarchies are shown in UML class diagrams
- Two children of the same parent are called **siblings**
- Common features should be kept as high in the hierarchy as possible
>[! tip] Key Concept
>Common features should be located as high in class hierarchy as is reasonable, in order to minimize maintenance efforts

![[Screenshot 2023-02-01 at 8.25.53 AM.png]]

### The `Object` Class
- In java, all classes are derived from the Object class
	- If not extension is defined, the object class is used by default
	- any public `Object` method can be called from any instanced object
	- The `toString` method is one such method

>[! tip] Key Concept
>All Java Classes are derived, directly or indirectly, from the Object class
>- The `toString` and `equals` methods are defined in the `Object` class and therefore are inherited by every class in every Java program
- Classes often override these basic methods in favor of a more appropriate definition

### Abstract Classes
- An abstract class represents a generic concept in a class hierarchy
- An abstract class cannot be instantiated and usually contains one ore more abstract methods
	- It can contain non-abstract classes and can contain data declarations other than constants

>[! tip] Key Concept
>An Abstract class cannot be instantiated. It represents a concept on which other classes can build their definitions 
---
>[! tip] Key Concept
>A class derived from an abstract parent must override all of it's parents abstract methods, or the derived class will also be considered abstract

### Interface Hierarchies
- The concept of inheritance can be applied to interfaces as well
- An interface can be derived from an interface
- When a parent interface is used to derive a child interface, the child inherits all abstract methods and constants of the parent.

>[! tip] Key Concept
>Inheritance can be applied to interfaces, so that one interface can be derived from another interface
- Class hierarchies and interface hierarchies do not overlap
- That is, an interface cannot be used to derive a class, and a class cannot be used to derive an interface

## B.15 Polymorphism
- The term `polymorphism` can be defined as "having many forms"
- A `polymorphic reference` is a reference variable that can refer to different types of objects at different points in time
>[! tip] Key Concept
>A polymorphic reference can refer to different types of objects over time

### References and Class Hierarchies
- a reference that is declared to refer to an object of a particular class also can be used to refer to an object of any class related to it by inheritance.
>[! example]
>if the class Mammal is used to derive the class Horse, then a Mammal reference can be used to refer to an object of class Horse.
>```java
>Mammel pet;
>Horse secretariat = new Horse();
>pet = secretariat
>```
- The reverse, assigning a horse to a mammal, is also possible, but requires an explicit declaration

>[! tip] Key Concept
>A reference variable can refer to any object created any class related to it by inheritance

### Polymorphism via Inheritance
>[! tip] Key Concept
>A polymorphic reference uses the type of the object, not the type of the reference, to determine which version of the method to invoke

### Polymorphism via Interfaces
- an interface name can be used as the type of a reference variable as well. An interface reference variable can be used to refer to any object of any class that implements that interface
>[! tip] Key Concepts
>An interface name can be used to declare an object reference variable. An interface reference can refer to any object of any class that implements the interface
>- Interfaces enable us to make polymorphic references, in which the method that is invoked is based on the particular object being references at the time
