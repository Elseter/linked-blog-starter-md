
---
aliases: [ "20221019110908",  ]
tags: RWU, COMSC, COMSC.110, Programming
date_created: 2022-10-19 11:09
---
[[COMSC.110 INDEX]]
# Objects and Classes
---
## Object Oriented Programming (OOP)
- An object represents an entity in the real world
- The <u>State</u> of an object consists of a set of data fields that represent its <u>properties</u> 
- The <u>Behaviors</u> of an object are defined by a set of <u>Methods</u>
## Classes
[[Inheritance]]
- Classes are templates that describe the shared properties and behaviors of an object
- May contain **Constructors**
	- Constructors are methods that have the same name as the class and have no return type
- Public variables and methods can be called anywhere
- Private variables/methods can only be used within the class
### Example of a class
```java
public class CircleRVK {  
  
    // no main() method  
    // 1 - data field: defines the properties of an object    
    // Private data types can not be accessed outside the class    
    private double radius;  
  
    // 2 - methods: defines the behavior of an object  
    // add the special method - Constructors: are methods,    
    // has same name as class, no return type    
    public CircleRVK(){  
        radius = 10.0;  
    }  
  
    // Overload the constructor  
    public CircleRVK(double r){  
        radius = r;  
    }  
  
    // Add Get Method  
    public double getRadius(){  
        return radius;  
    }  
  
    // Add Set Method  
    public void setRadius(double r){  
        radius = r;}  
  
    // Define a method to calc area of the circle  
    public double getArea(){  
        return Math.PI * Math.pow(radius, 2);  
    }  
}
```
### Example of creating an object
```java
public class CircleDriverRVK {  
    public static void main(String[] args){  
  
        // Create the first circle object  
        // Calling original constructor to create first object       
         CircleRVK circle = new CircleRVK();  
         
        // Prints 10.0, the size set by default constructor  
        System.out.printf("The radius of circle 1 is %.2f%n", circle.getRadius());  
  
        // Create the second circle object by calling the  
        // Overloaded Constructor        
        CircleRVK circle2 = new CircleRVK(25);  
        System.out.printf("The radius of circle 2 is %.2f%n", circle2.getRadius());  
        
        // Test set method  
        circle2.setRadius(100);  
        System.out.printf("The radius of circle 2 after calling" +  
                " set method is %.2f%n", circle2.getRadius());  
  
    }  
}
```
### Accessing Object's members
- Referencing the objects data:
		objectRefVar.data
		myCircle.radius
- Invoking the object's method:
		objectRefVar.methodName(*arguments*)
		myCircle.getArea()

### Static V.S Non-Static Methods
- Static methods are those that are defined by a <u>constant and unchanging key-name</u>
		IE. Math.PI
- Non-Static methods are methods that are invoked from objects 
		IE. myCircle.getArea()

### Data Types
**Null Value**
- If a data field of a reference type does not reference an object, the data field holds a special literal value, null

**Default Value for a Data Field**
| Data Type | Default Value |
| --------- | ------------- |
| Reference | null          |
| Numeric   | 0             |
| Boolean   | false         |
| Char      | 'u0000'       |
- java assigns no default value to a local variable inside a method

**Instance Variables**
- Instance variables can only be accessed within that specific instance of the object
**Static**
- Static variables are shared by all instances of the class
- Static variables are not tied to a specific instance of an object
- Static methods are not tied to a specific object
- Static constants are final variables shared by all the instances of the class

### Copying Variables/Objects
![[COMPSCI.110 Object Copying.png]]
- This is why objects are known as reference type. Objects reference a piece of memory. Setting one object equal to another simply <u>changes it's reference location</u>
- This means that future changes to c1 or c2 will change BOTH

#### Garbage Collection
- As shown in the previous figure, after the assignment statement c1 = c2, c1 points to the same object referenced by c2. 
- The object previously referenced by c1 is no longer referenced. This object is known as garbage. Garbage is automatically collected by JVM. 

### Visibility modifiers
*public*
- The class, data, or method is visible to any class in any package
*private*
- The data or methods can be accessed only by declaring the class
*default*
- The default modifier allows access within the same package, but not outside that package

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
