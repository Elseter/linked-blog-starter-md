
---
aliases: [ "20221223132922",  ]
tags: C++, Programming
date_created: 2022-12-23 13:29
---
[[C++ Index]]
# A C++ Hello World 
---
## A Minimal Program
>[! tip] The Most Minimal Program
>```cpp
>int main() { } // comment
>```
- This function defines the main, which takes no arguments and does nothing
	- { } indicate the body of the function
	- // indicate the beginning of a comment line
- EVERY C++ program must have exactly one global function called *main*
- The int value returned by main, if any, is the programs return value to the system
	- Any non-zero value indicates failure
	- Not all systems take advantage of that return value
		- Often linux/Unix-based systems do, Windows do not

## Hello World
>[! tip] Hello World
>```cpp
>include <iostream\>
>
>int main() 
>{
>	std::cout << "Hello World!\n"
>}
- Ignore the additional \\ in <iostream\>
- the operator << ("put to") writes a second argument into the first
	- In this case, the string literal "Hello World!\n" is written into the standard output stream std::cout
	- std:: specifies that the name cout is from [[Introduction to C++#The Standard Library|The Standard Library]] 
- C++ 20 has added the import feature, but at the time of note taking, It is not implemented on my machine, so I will be using the old # include statements

## Final Example 
```cpp
#include <iostream>

// make then names from std visable without the inclusion of std::
using namespace std;

// function that finds the square of its input
double square(double x){return x*x;}

// function that prints the square of its input
void printSquare(double x)
{
    cout << "The square of " << x << " is " << square(x) << "\n";
}
int main() 
{
    printSquare(4);
}
```
