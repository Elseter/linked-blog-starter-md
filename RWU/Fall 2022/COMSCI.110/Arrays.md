
---
aliases: [ "20221021105733",  ]
tags: RWU, COMSC, COMSC.110, Programming
date_created: 2022-10-21 10:57
---
[[COMSC.110 INDEX]]
# Arrays
---
## Single Dimensional Arrays

### What is an Array
- An <u>array is a data structure that represents a collection of the same data types</u>
- Use **ONE** name to refer to a collection of data
	- This data must be the same type, must be primitive data type
``` java
// Array Structure
datatype arrayRefVar[];

//Creating an Array
datatype array = new datatype[arraysize]
// Example
double mylist[] = new double[5]; // 
```
### Length of an Array
- Once created, the size of the array is <u>fixed</u>. It cannot be changed
- You can find the size by using 
```java 
 arrayRefVar.length
```
### Default Values
- When an array is created, its elements are assigned default values unless specified otherwise
		- **0** for numeric primitive data types
		- '$\u0000$' for char types
		-  **false** for boolean types

### Indexed Variables
- The array is a <u>0-based index</u> 
- Starts at 0 and ends at array.length() - 1
- Each element in the array is represented using the following syntax as an **==indexed variable==**
```java
arrayRefVariable[index];
```
#### Work From Class
```Java
public class ArrayTestRVK {  
    public static void main(String[] args){  
  
        // Declare an array  
        int[] myData = new int[5];  
  
        // Assign variables into array  
        myData[0] = 1;  
        myData[1] = 2;  
        myData[2] = 3;  
        myData[3] = 4;  
        myData[myData.length - 1] = 5;  
  
        //add content  
        myData[0] = myData[myData.length-1] + myData[myData.length-2];  
  
        // declare new array  
        int[] myData2 = new int[5];  
  
        // fill array2  
        for(int i = 0; i < myData2.length; i++){  
            myData2[i] = i+1;  
        }  
        // Print array2  
        for(int i = 0; i < myData2.length; i++)  
            System.out.println(myData2[i]);  
  
        // MORE CLASS EXERCISES  
        //Problem 1: Reset whole array with value of 111        System.out.println("\nProblem 1");  
        for(int i = 0; i < myData.length; i++) {  
            myData[i] = 111;  
            System.out.println(myData[i]);  
        }  
        // Problem 2: random numbers  
        System.out.println("\nProblem 2");  
        for(int i = 0; i < myData.length; i++) {  
            myData[i] = (int)(Math.random()*66);  
            System.out.println(myData[i]);  
        }  
        // Problem 3: Add 10 to each  
        System.out.println("\nProblem 3");  
        for(int i = 0; i < myData.length; i++) {  
            myData[i] += 10;  
            System.out.println(myData[i]);  
        }  
  
    }  
}
```