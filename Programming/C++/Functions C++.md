
---
aliases: [ "20221223145319",  ]
tags: C++, Programming
date_created: 2022-12-23 14:53
---
[[C++ Index]]
# Functions C++
---
## Functions
- The main way to accomplish things in c++ is through calling functions
- A function can not be called unless it is clearly declared in a place that the compiler can recognize
>[! info] Declaring a Function
>A function declaration gives the name of the function, the type of value returned (if any), and the number/types of arguments that must be supplied in a call. For Example
>```cpp
>Elem next_elem(); \\no argument, return a pointer to Elem (object)
>void exit(int); \\int argument, return nothing
>double sqrt(double); \\double argument, return a double

### Arguments
- A function declaration may declare argument names, but it is not required unless you wish to reference them in the function declaration body

### Function Types
>[! tip] Function types
>The type of a function consists of its return type followed by the sequence of its arguments within parenthesis. 
>Functions can also be members of a class. These are called **Member Functions**
>- For these functions, the name of its class is also part of the function type
```cpp
double get(const vector<double>& vec, int index);
// type: double(const vector<double>, int)

char& String::operator[](int)
// type: char& String::(int)
```
### Overloading a Function
>[! definition] Overloading
>Defining multiple functions with the same name is known as **function overloading** and it is an essential part of generic programing. Ex 
>```cpp
>void print(int);
>void print(double);
>void print(string);
>
>int main()
>{
>print(42);       // calls print(int)
>print(9.65);    // calls print(double)
>print("Test")  // calls print(string)
>}
>```
- If this is left two ambiguous, where two functions could be reasonably called, this will result in an error