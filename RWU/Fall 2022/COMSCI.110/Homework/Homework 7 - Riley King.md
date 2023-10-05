
---
aliases: [ "20221115122725",  ]
tags: RWU, COMSC.110, COMSC, Homework
date_created: 2022-11-15 12:27
---
[[COMSC.110 INDEX]]
# Homework 7 - Riley King
---
## Assignment
[[COMSC.110 HW7.pdf]]

## Completed Work
### Question 1
1. (5 pts) Given the class defined at the end of this question: 
		a. How many constructors does the class have?
		b. Name one local variable used somewhere in the class.
		c. How many static class variables are defined? List their names.
		d. How many instance class variables are defined? List their names.
		e. How many instance methods are defined? List their names. 
		f. How many static methods are defined? List their names. 
		g. Write one line of code to create an object using the constructor of your choosing. 
		h. Write one line of code to invoke the static method of your choosing. 
		i. Write one line of code to invoke the instance method of your choosing
#### Question 1 Code
```java
class B { 
	int x = 0;
	int y; 
	static int z = 10; 

	B(){y = x; z--; } 
	 
	B(int y){
	  this.y = y; z--; } 
	  
	B(int y, int x){ 
		this.y = y; 
		this.x = x; 
		z--; } 
	
	void c(){ 
		String s = "Sum = "; 
		System.out.println(s + (x + y + z)); } 
	
	double d(double a){
		double b = Math.sqrt(a); 
		return b + x + y + z; } 
	
	static int e(){ 
		int x = 10; 
		return Math.abs(z - x); } 
	
	static boolean f(int n){ 
		return z > n; } 
	
	int g(){ return x; } }
```
#### Answer of Question 1
>[!done] Answers for 1
>a. The class has 3 constructors. 1 Default and 2 overloaded
>b. double b is a local variable that has a scope that is only present in method d
>c. There is only **one** static variable, which is int z = 10;
>d. There are **two** instance variables, which are int x = 0; and int y;
>e. There are three instance methods. 
>	void c()
>	double d()
>	int g()
>f. There are two static methods
>	static int e()
>	static boolean f()
>g. 
>``` java
>B instanceOfB = new B();
>```
>h. 
>```java
>if(B.f(6)){
>}
>```
>i. 
>```java
>instanceOfB.c();
>```

### Question 2
(5 pts) What’s the output of the following code:
#### Question 2 Code
```java
public class Test {
	public static void main(String[] args) {
	
		A a1 = new A();
		a1.addOne(); 
		System.out.println(a1.i); 
		System.out.println(a1.j); 
		
		A a2 = new A(); 
		a2.addOne(); 
		System.out.println(a2.i); 
		System.out.println(a2.j); 
	} 
} 
class A {
	int i = 100;
	static int j = 0;
	
	A(){ 
	} 
	
	void addOne(){ 
	i++;
	j++; 
	} 
}
```
#### Answer for Question 2
>[! done] Answers for 2
>The code above will print the following to the console:
>```java
101
1
101
2
>```

### Question 3
(5 points) Suppose you wanted to define the following classes using inheritance: Cat, Bird, Animal, Mammal, Dog, Owl. Write the class definition headers that you would use. For example, if the problem were to define the classes Circle, Triangle, and Shape, the solution would be: 
#### Question 3 Code
```java
class Shape
class Circle extends Shape 
class Triangle extends Shape
```
#### Answer for Question 3
>[! done] Answers for 3
>```java
>class Animal
>class Mammal extends Animal
>class Cat extends Mammal
>class Dog extends Mammal
>class Bird extends Animal
>class Owl extends Animal
>```

### Question 4
(5 points) For each of the following state whether or not it could be compiled without error. Assume the Circle class is a subclass of the Shape class (Circle extends Shape).
#### Question 4 Code
```java
a. Shape s = new Circle(); 

b. Circle c = new Shape(); 

c. Shape s = new Shape(); 
Circle c = s; 

d. Circle c = new Circle();
Shape s = c; 

e. Shape s = new Shape();
Circle c = (Circle)s;
```
#### Answer for Question 4
>[! done] Answers for 4
>a. Part A <u>will compile</u> without issue. 
>b. Part B <u>will NOT compile</u>. Shape is the parent class and may not contain the necessary components to create a circle object
>c. Part C <u>will NOT compile</u>.
>d.  Part D <u>will compile</u>
>e. Part E <u>will compile</u> as the appropriate casting has been done

### Question 5
(3 points) In question 2, how many objects are created in total (in all of parts a through e)? How many Circles? How many Shapes?

#### Answer for Question 5
>[! done] Answers for 5
>I'm assuming that the question is referring to the code in question 4, not question 2.
>- In Part A, a new circle object is created and then cast into a shape object
>- In Part B, a new shape object is created, however, it is unsuccessfully cast into a circle
>- In Part C, a new shape object is created, then this shape unsuccessfully cast into a circle
>- In Part D, a new circle object is created, then cast into a shape object
>- In Part E, A new shape object is created, then successfully cast into a Circle object

| Object | Part A | Part B | Part C | Part D | Part E | Total |
| ------ |:------:|:------:|:------:|:------:|:------:|:-----:|
| Shape  |   1    |   1    |   1    |   1    |   1    |   5   |
| Circle |   1    |   0    |   0    |   1    |   1    |   3   |
| TOTAL  |   2    |   1    |   1    |   2    |   2    |   8   |


### Question 6
(3 points) How could you change the printInfo method in class B to use the super keyword?

#### Question 6 Code
```java
public class A { 
	void printInfo(){
		System.out.println("Information from class A"); 
	} 
} 

class B extends A { 
	void printInfo(){ 
		System.out.println("Information from class A"); 
        System.out.println("Information from class B"); 
    } 
}
```

#### Answer for Question 6
>[! done] Answers for 6
>```java
>class A {  
>    public A(){ }     
>    void printInfo(){  
>        System.out.println("Information from class A");  
>    }  
> }  
 > 
>class B extends A {  
>    public B(){ }  
>    void printInfo(){  
>        super.printInfo();  
>        System.out.println("Information from class B");  
>    }  
>}
>```


### Question 7
(3 points) Given the following code, what will be printed? (If you aren’t sure you may want to type it in.)

#### Question 7 Code
```java
public class Test{
	public static void main(String[] args){ 
		new A(); 
		new B(); 
	} 
} 

class A { 
	int num = 1; 
	public A(){ 
		System.out.println("A's constructor is invoked"); 
	} 
	public void setNum(int i){ 
	num = 2 * i;
	} 
} 

class B extends A {
	public B(){ 
		System.out.println("B's constructor is invoked"); 
	} 
}
```
#### Answer for Question 7
>[! done] Answers for 7
>The code above will print the following to the console
>```java 
>A's constructor is invoked
A's constructor is invoked
B's constructor is invoked
>```

### Question 8
(6 points) Refer to the code in question 5 
		a. Suppose you wanted to write a method in class B to override the setNum method. What would the method header be? 
		b. Give a method header that could be used in class B to overload the setNum method or state that it is not possible.

#### Answer for Question 8
>[! done] Answers for 8
>a.  
>```java
>class B extends A {  
>    public B(){  
>        System.out.println("B's constructor is invoked");  
>    }  
>    @Override  
>    public void setNum(int i){  
>        // code you wish to run when setNum is invoked from an instance of B  
>    }  
>}
>```
>b. To overload the method, you use the same name, but change the dummy parameters 
>```java
>class B extends A {  
>    public B(){  
>        System.out.println("B's constructor is invoked");  
>    }  
>    public void setNum(double i){  
>        // code you wish to run when setNum is invoked from an instance of B  
>    }  
>}
>```

