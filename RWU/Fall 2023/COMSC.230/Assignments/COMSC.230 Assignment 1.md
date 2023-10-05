---
aliases:
  - '[ "20230919102435",  ]'
tags:
  - COMSC
  - COMSC230
date_created: 2023-09-19 10:24
Index: "[[COMSC.230 Index]]"
---

# COMSC.230 Assignment #1
---
- Due Wednesday 9/20/2023

1. Given the following assembly language instructions format and initial registry values, execute the provided set of instructions. Show your execution using binary number operations and update the registers using hexadecimal representations (need to show final content for all registers):
	![[Screenshot 2023-09-19 at 10.27.02 AM.png]]
![[2023-09-19 10-45_page_1.jpg]]

2. Given the simple grammar 
	G: 
	< exp > ::= < exp > ∗ < exp > | < exp > / < exp > 
	< exp > ::= | < exp > && < exp > 
	< exp > ::= < mathFunc > 
	< exp > ::= (exp)|x|y|z 
	< mathFunc > ::= mod(< exp >, < exp >)|fib(< exp >, < exp >)|xor(< exp >, < exp >) 
	
	**Do the following problems:**
	1. Derive at least three strings that belong to the language L(G). Show your derivations.
	2. Use syntax diagrams (directional graphs) to show the production for each non-terminal symbol. Hint: The answer should be presented with two diagrams, one for < exp > and for < mathFunc >.
![[2023-09-20 09-49_page_1.jpg]]

3. Given the grammar C:
< assigmnet − stmt >::=< identif ier >=< exp >; 
< exp >::= | < exp > ∗ < exp > | < exp > + < exp > | < exp > − < exp > |(< exp >) | < identif ier > | < integer > 
< identifier >::= x|y|z 
< integer >::= 1|2|3|4|5|6|7|8|9... (all the integers)

Generate the Parse Trees for the following sentences for the language L(C) :
1. y = x + 22; 
2. y − z ∗ (x ∗ x) − 360
![[2023-09-20 09-52.jpg]]

4. Briefly describe the difference between syntax and logical errors; In addition, provide an example of each type of error using a programming language code as reference (use any language you want).

>[! answer] Answer for 4
>A syntax error occurs when the typed expression does not match any of the possible sentences within a language as defined by that languages grammar. This can be as simple as misspelling a language defined variable, or missing a semi-colon to indicate structure in certain languages. 
>```c++
>int main()
>{
>	int y, x, z;
>	if (x == y)
>	{
>		std::cout << x << " is equal to " << y << std::endl;
>		sd::cout << "Program finished";
>	}
>	return 0;
>}
>```
>In the example above, the programming makes a simple spelling error by forgetting the 't' in std on the second to last line. This would result in the compiler being unable to locate the function sd::cout as it likely doesn't exist or if it does, it serves a very different function.
>
>A logical error isn't always an error per say, however, your program is returning a result that is not intended. The most common example of this that is often seen among new programs is a misunderstand of type casting. 
>```c++
>using namespace std;
>int main()
>{
>	int x, y;
>	cout <<  x/y << endl;
>}
>```
>The example above will compile and run just about every time, with the exception of y=0. However, if the program needs the result to be accurate to any decimal, the program above will result in a logical error as it uses integer division. The result of x/y that is sent to the cout function will be rounded down to the nearest integer. This is an intended part of integer division, but can cause logical errors when not accounted for.

