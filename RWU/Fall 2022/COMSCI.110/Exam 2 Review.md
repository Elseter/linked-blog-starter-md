
---
aliases: [ "20221102110654",  ]
tags: RWU, COMSC.110, COMSC, Programming, ExamReview
date_created: 2022-11-02 11:06
---
[[COMSC.110 INDEX]]
# Exam 2 Review
---
## Strings and Characters
\ <u>+ operator</u>
	- used to concatenate strings
	- Strings are essentially lists of chars and you are adding to the end of that list
<u>Escape Sequences</u>
	- by using a \ you can escape characters 
	\\t, \\n, \\", \\'

## Conditional statements 
### if, if-else, switch statements
```java
// if statement
if (condition){
	// code that runs if/while condition is met
}

if (condition){}
else {
// Code that runs if the if statement is not met
}

// SWITCH STATEMENT
switch (expression){
	case value1:
		// code that runs if expression matches value1
		break;
	case value2:
		// code that runs if expression matches value2
	...
	
	default:
		// code that runs if expression does not match any of the values
}
// Enchanced Switch Statements (break statements not required)
switch(expression){
	case value1 -> // code that runs when expression = value1
	case value2 -> // code that runs when expression = value2
	...
	default -> // code that runs wehn expression != value
}
```
### Conditional Operator
```ad-note
```java
(Condition) ? // code that returns when true : code that returns when false;
```
```ad-done
```java
int largest = (n1>n2) ? ((n1>n3) ? n1 : n3) : ((n2>n3) ? n2 : n3);
```

## Repetition Statements
### While, Do-While, For Loops
```java
// While statement
while (boolean condition){
// code that runs while condition is true
}

// Do while
do{
// Code that runs once first
// Then runs while the condition at the end is met
}
while (boolean condition);

// For Loop
for (statement 1; statement 2; statement 3){
	Statement 1 // runs one time before the execution of the code block
	Statement 2 // defines the condition for executing the code block
	Statement 3 // is executed every time after block
}
for (int i =0; i<5; i++){
	System.out.println(i)
}
```
## Arrays
[[Arrays]]
### Declarations
```java
double[] array = new double[arraySize];
double[][] array = new double[arraySize1][arraySize2]
```
- numeric types are generated with value **0 or 0.0**
- booleans are generate **false**
- objects are generate as **null**
### What is an Array
- An <u>array is a data structure that represents a collection of the same data types</u>
- Use **ONE** name to refer to a collection of data
	- This data must be the same type, must be primitive data type
- <u>Once created, an array's size is fixed</u>

## Classes and Objects
[[Objects and Classes]]
### Objects
- An object represents an entity in the real world
- The <u>State</u> of an object consists of a set of data fields that represent its <u>properties</u> 
- The <u>Behaviors</u> of an object are defined by a set of <u>Methods</u>
- AN INSTANCE OF A CLASS
### Classes
- A class is a template that describes the shared properties and behaviors of an object
- May contain **Constructors**
	- Constructors are methods that have the same name as the class and have no return type
### Data Accessibility
*public*: The class, data, or method is visible to any class in any package
*private*: The data or methods can be accessed only by declaring the class
*default*: The default modifier allows access within the same package, but not outside that package
### Static V.S non-Static
Static methods are those that are defined by a <u>constant and unchanging key-name</u>
		IE. Math.PI
- Non-Static methods are methods that are invoked from objects 
		IE. myCircle.getArea()
Static means class wide... Non-Static means instance specific 
### This Keyword
- The <u>this</u> keyword is the name of a reference that refers to an object itself. One common use of the <u>this</u> keyword is to reference a class's *hidden data fields*
- Another common use of the <u>this</u> keyword is to enable a constructor to invoke another class
```java
public CircleRVK(double radius){  
    this.radius = radius;  
    numberOfObjects++;  
}  
//overloaded constructor  
public CircleRVK(){  
    this(10);  
}
```
## Parameters 
Formal Parameters : used in method definition
Actual Parameters : used when method is called