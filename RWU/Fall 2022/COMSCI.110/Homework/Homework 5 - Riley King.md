
---
aliases: [ "20221101095834",  ]
tags: RWU, COMSC.110, COMSC, Homework
date_created: 2022-11-01 09:58
---
[[COMSC.110 INDEX]]
# Homework 5 - Riley King
---
## Assignment
[[COMSC.110-HW5.pdf]]

## Completed Work
1. Which of the following are valid declarations, and why?
		a. int primes = {2,3,4,5,7,11}; 
		b. int[] scores = int[30];
		c. int[] primes = new { 2,3,4,5,7,11}; 
		d. int[] scores = new int[30];

```ad-done
title: Question 1 ANSWER
	A. int primes = {2,3,4,5,7,11} is NOT a vaild declaration. The varaible primes is declared as a solitary primative int whereas it is being fed an object data type (list). Additionally 4 isn't a prime 😉

	B. int[] scores = int[30] is NOT a valid declaration. It is missing the new object declaration. 

	C. int[] primes = new {2,3,4,5,7,11} is NOT a valid declaration. You do not need to declare a list as a new object when you are directly supplying the data values within the list in the format used above.

	D. int[] scores = new int[30] IS A VALID declaration. The int[] type is in the correct format. The new object is properly declared and the list size is set approperatly.
```


2. Write an array declaration to represent the following statements 
		a. students’ names for a class of 25 students 
		b. students’ test grades for a class of 40 students (letter grades)
		

```ad-done
title: Question 2 ANSWER
**Part A**
```java
Scanner scan = new Scanner(System.in);  
System.out.println("Enter Student Names: ");  
  
String[] names = new String[25];  
for (int i =0; i< names.length; i++)  
    names[i] = scan.nextLine();
```

``` ad-done
title: Question 2 ANSWER
**Part B**
```java
Scanner scan = new Scanner(System.in);  
System.out.println("Enter Student Grades: ");  
  
char[] grades = new char[40];  
for (int i =0; i< grades.length; i++)  
    grades[i] = scan.next().charAt(0);
```


3. What’s the value of the array data after following the following java code fragment:
			*I've altered the code slightly, the final references an array called values, however, there is no values array declared in the code. I've treated the <u>values</u> as if they were intended to be <u>data</u>. unchanged this would just result in data[0] = 0*
```java
public class Test{ 
	public static void main(String[] args){ 
		int[] data = new int[6]; 
		for (int i = 1; i < 6; i++){ 
			data[i] = 3*i + data[i-1]*2; 
			} 
		values[0] = values[1] + values[4]; 
	} 
}
```
```ad-done
title: Question 3 ANSWER
```java
data[0] = 81
data[1] = 3
data[2] = 12
data[3] = 33
data[4] = 78
data[5] = 171
```


4. Show the output of the following code:
		*Again an unknown variable is referenced, I've changed this to be data*
```java
int[][] data = {{1,2}, {3,4}, {5,6}};
int sum = 0;
for (int i=0; i<data.length;i++){
	sum += data[i][0];
}
System.out.println(sum);
```
```ad-done
title: Question 4 ANSWER
The output of the code above will be 9. The code adds the first item in each of the nested lists to each other, then prints this sum to the console.
```
