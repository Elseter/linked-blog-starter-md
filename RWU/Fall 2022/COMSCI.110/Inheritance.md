
---
aliases: [ "20221107110458",  ]
tags: RWU, COMSC.110, COMSC, Programming
date_created: 2022-11-07 11:04
---
[[COMSC.110 INDEX]]
# Inheritance
---
# Inheritance
- Allows a software developer to derive a new class from an existing one
- The existing class is called the **parent class** or **superclass**
- The new class is called the **child class** or **subclass**
	- The child class inherits characteristics of the parent class
	- <u>inherits methods and data defined by parent class</u>

### Unified Modeling Language
- Inheritance relationships are shown in UML class diagram
	- use a solid arrow with unfilled triangular arrowhead pointing to the parent class

Proper Inheritance creates an <u>is-a</u> relationship
	The child **is a** more specific version of the parent

### Inheritance
- can add new variables or methods
	- or can modify the inherited ones
- <u>Software Re-use</u> is a fundamental benefit of inheritance 
	- Capitalize on existing effort, design, implementation and testing of existing software

### Deriving Subclasses
- In Java, we use the reserved word *extends* to establish an inheritance relationship
>[!code] Subclass Declaration
>```java
>class Car extends Vehicle
>{
>\\ class contents
>}
>```

### Protected Modifier
- protected in a visibility modifier
- variables and methods declared with <u>private</u> can not be referenced by name in ==child class==
- <u>protected variables</u> allow a child class to reference a variable or method from a parent class
	- Visible in same package
	- Provides more encapsulation

## Are Superclass's Constructor Inherited
- NO
- They are invoked explicitly or implicitly
- Explicitly using the *super* keyword... super();
- if the keyword <u>super</u> is not explicitly used, the superclass's no-arg constructor is automatically invoked
- super can be used to get methods... IE super.getColor()

### Trace Execution
```java
pubilc class Faculty extends Employee{
	public static void main(String[] args){
		new Faculty();
	}

	public Faculty(){
		System.out.println("(4) Faculty's no-arg constructor is invoked");
	}
}

public Employee extends Person{
	public Employee(){
		this("(2) Invoke Employee's overloaded constructor");
		System.out.println(" (3) Employee's no-arg constructor is envoked");
	}

	public Employee(String s){
		System.out.println(s);
	}
}

class Person {
	public Person {
		System.out.println("(1) Person's no-arg constructor is invoked")
	}
}
```
## Method Overloading V.S Method Overriding
### Method Overloading
- Same name
- Different signature
### Method Overriding
- Same name
- Same signature
- Only in Inheritance
	- Changed within the child class
>[!note] NOTE
>An instance method can only be overridden if it is accessible. Thus **a private method cannot be overridden**

>[!note] NOTE Cont.
>Like an instance method, a static method can be inherited. However ** a static method cannot be overridden**

## The Object Class
- Every class in java is descended from <u>java.lang.Object class</u>
	- If no inheritance is specified, the superclass if Object

## To String Method
```java
toString();
```
- by default this is Classname@number
	- Usually you override this to provide a more descriptive/digestible representation of the object

