
---
aliases: [ "20221022220241",  ]
tags: RWU, COMSC.110, COMSC, Homework
date_created: 2022-10-22 22:02
---
[[COMSC.110 INDEX]]
# Homework 4 - Riley King
---
## Assignment
[[COMSCI.110_HW4.pdf]]

## Completed Work
1. Evaluate the following code fragment and figure out what will be printed out. 
``` java
int i = '1'; 
int j = '5' + '2' * ('9'-'3') + 'c'/'a'; 
int k = 'a'; 
char c = 90; 
System.out.println(i + " " + j + " " + k + " " + c);
```
![[ASCII-Table.jpg]]

**Result**
	The code above will print ==49 354 97 Z== to the console (Not highlighted when printed)

2. Evaluate the following code fragment and figure out what will be printed out. 
```java
char x = 'm';
char y = 'o';
System.out.println(++x);
System.out.println(y++); 
System.out.println(x-y);
```
**Result**
	The above will print what follows to the console:
	
	n
	o
	-2

3. Evaluate the following code fragment and figure out what will be printed out.
 ``` java
String s1 = "Columbus Day Holiday";
String s2 = "Hollaween"; 
String s3 = "Columbus Day Holiday"; 

System.out.println(s1.equals(s2));
System.out.println(s1.equals(s3));
System.out.println(s1.compareTo(s2));
System.out.println(s1.compareTo(s3));
System.out.println(s1.charAt(1)); 
System.out.println(s1.indexOf('D')); 
System.out.println(s1.substring(9,13)); 
System.out.println(s1.concat(s2));
```
**Result**
	The above will print what follows to the console:
	
	false
	true
	-5
	0
	o
	9
	Day 
	Columbus Day HolidayHollaween

4. Let str1 be “ Welcome” and str2 be “ welcome”. Write java code for the following statements:
		a. Check if str1 is equal to str2 and assign the result to a boolean variable isEqual; 
		b. Check if str1 has the prefix of A and assign the result to a boolean variable b; 
		c. Assign the length of str1 to an int variable x; 
		d. Create a new string str3 which combines str1 and str2; 
		e. Create a substring of s1(Q3) from index 9 to the end; 
		f. Create a new string str4 which converts str1 to uppercase
```java
public class TEMPLATE {  
    public static void main(String[] args){  
        String str1 = "Welcome";  
        String str2 = "welcome";  
        String s1 = "Columbus Day Holiday";  
  
        boolean isEqual = str1.equals(str2);  
        boolean b = str1.charAt(0) == 'A';  
        int x = str1.length();  
        String str3 = str1.concat(str2);  
        String s1Sub = s1.substring(9);  
        String str4 = str1.toUpperCase();  
  
        System.out.println(isEqual);  
        System.out.println(b);  
        System.out.println(x);  
        System.out.println(str3);  
        System.out.println(s1Sub);  
        System.out.println(str4);
```
5. Indicate the output that will be produced. Assume the following declarations are made just before each exercise. That is, assume these initializations are in effect at the beginning of each problem: 
```Java
final int MIN = 10, MAX = 20;
int num = 15;

a)while (num < MAX){ 
   System.out.println (num); 
   num = num - 1; } 
 
b)do{ 
   num = num + 1; 
   if (num*2 > MAX+num) 
      System.out.println (num); } 
  while (num <= MAX); 

c)for(int count1=1; count1 <= 6; count1++){ 
   for (int count2=1; count2 <= 3; count2++) 
     System.out.print("#"); 
   System.out.println(); }
```
a. The code presented in a) will result in an <u>infinite while loop</u>, as num will constantly be shrinking with no chance for it ever to exceed MAX

b. The code presented in b) will print ==21== to the console

c. The code presented in c will print 6 rows of 3 hashtags per row like such,
```Java
###
###
###
###
###
###
```

