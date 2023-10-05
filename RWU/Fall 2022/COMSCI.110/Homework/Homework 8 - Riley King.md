
---
aliases: [ "20221212093013",  ]
tags: RWU, COMSC.110, COMSC, Homework
date_created: 2022-12-12 09:30
---
[[COMSC.110 INDEX]]
# Homework 8
---
## Assignment
[[COMSC.110 HW8.pdf]]

## Completed Work
### Question 1
1. Given the following
		a. If no exception occurs which lines will execute? 
		b. If line2 causes an exception of type ExceptionType1, which lines will execute? 
		c. If line2 causes an exception of type ExceptionType2, which lines will execute?

#### Question 1 code
```java
try{ 
	line1; 
	line2; 
	line3; 
} 
catch(ExceptionType1 e){
	line4; 
} 
finally{ 
	line5; 
} 
line6;
```
#### Answer for Question 1
>[! done] Answer for 1
>a. If no exception occurs, then the following lines within the try, and finally blocks will run. Followed by the code outside of the block. Lines 1, 2, 3, 5, and 6 will run.
>
>b. If line2 causes and exception of ExceptionType1, Lines 1, 2, 4, 5, and 6 will run. That said, line 2 may be interrupted and may not complete in the intended manner.
>
>c. If line2 cases an exception of ExceptionType2, you receive an interesting result. I wasn't entirely sure how the finally block would work, so I ran this through my IDE. It resulted in lines 1, 2, and 5 being run, followed the the exception being printed to the console. Line 2 was also not fully completed as I had intended for it to print something to the console.
>
![[COMSC.110 screenshot.png]]

### Question 2
2. What exceptions will the following pieces of code throw (try them out if you aren’t sure)?

#### Question 2 Code
```java
a. int[] myArray = new int[10]; 
   System.out.println(myArray[10]); 
   
b. System.out.println(1 / 0); 

c. Object o = new Object();
   String d = (String)o; 
   
d. Object o = null;
   System.out.println(o.toString());
```
#### Question 2 Answer
>[! done] Answer for 2
>a. Part a will throw an IndexOutOfBounds Exception. Arrays are 0 based and only has 10 elements. In the second line, you reference an eleventh item that does not create in memory.
>
>b. Part b will throw an Arithmetic Exception as division by 0 is impossible
>
>c. Part c will throw a ClassCast Exception as you cant cast an Object into a String
>
>d.  Part d will throw a NullPointer Exception as you cant call .toString() on a null object

### Question 3
3. True or false and why?
		a. An abstract class can be used just like a non-abstract class except that you cannot use the new operator to create an instance from the abstract class. 
		b. An abstract class can be extended. 
		c. A subclass of a non-abstract superclass cannot be abstract. 
		d. A subclass cannot override a concrete method in a superclass to define it as abstract. 
		e. An abstract method must be non-static.

#### Question 3 Answer
>[! done] Answers for 3
>a. Abstract classes are defined by the fact that they contain abstract methods that are not implemented. They differ from normal classes as be can not create objects from them. True
>
>b. False. you must create a child class or implement all methods
>c. False
>d. False
>e. True

### Question 4
4. Show the error in the following code:

#### Code for Question 4
```java
interface A {
	void m1(); 
} 
class B implements A { 
	void m1() {
		System.out.println("m1"); 
	} 
}
```
#### Answer for Question 4
>[! done] Answer for 4
>```java
>interface A {  
>    void m1();  
>}  
>class B implements A {  
 >   public void m1() {  
>        System.out.println("m1");  
 >   }  
>}
>```
>m1() in class B clashes with m1() in A. So I've assigned different privileges through public to avoid this clash.

### Question 5
5. Which of the following is the correct method header for the compareTo method in the String class?
```java
public int compareTo(String o) 
public int compareTo(Object o)
```

#### Answer for Question 5
>[! done] Answer for 5
>```java
>public int compareTo(String o)
>``` 

### Question 6
6. Can the following code be compiled? Why?

#### Code for Question 6
```java
Integer n1 = new Integer(3); 
Object n2 = new Integer(4); 
System.out.println(n1.compareTo(n2));
```
#### Answer for Question 6
>[! done] Answer for 6
> This will NOT compile. In line 2, it attempts to convert and Object into an Integer. However, these are incompatible types.  

