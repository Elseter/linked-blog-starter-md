---
aliases:
  - '[ "20230918153634",  ]'
tags:
  - COMSC
  - COMSC230
date_created: 2023-09-18 15:36
Index: "[[COMSC.230 Index]]"
---

# COMSC.230 Lecture 4
---
## Lecture Topics
- What is Imperative/Structural programming

### What is imperative programming?
- Programs consist of routines containing instructions that are executed mostly in sequence
- Control structures, such as decisions and cycles, and calls to subprograms (routines) are used to alter the sequence
- Based on the latter, imperative programming is also known as structured and also as procedural
- Object orient programming can be considered imperative
- The state of a program can be determined by observing the values of the variables
- The imperative praradigm is deeply rooted in the concept of Von Neumann architecture. This is seen by many as a negative aspect that makes programming difficult
- Languages such as Basic, C, Cobol, Fortran, and Pascal

### The difference between Imperative, Procedural and Structured 
- **Imperative**
	- Describes a series of commands (or statements) for the computer to execute
	- step by step
- **Structured**
	- All units of work should be broken into smaller tractable parts - functions to be re-used

#### Von Neumann
- Mathematician John Von-Neuman designed the specification for the first programmable computer in 1954, where the programs themselves could be stored in memory, not just data
	- Fetch an instruction
	- Decode the instruction
	- Execute the instruction

### Structured Programming
- The emphasis on the structure and correctness of an imperative program should be independent of its efficiency
- An unstructured program can be as efficient (or more) than a structured program
- The advantage of structured programming is that is allows subprograms to be reused and these subprograms are easier to modify and improve
- A program is structured if the control flow of a program is evident given the syntactic structure of the source code
- Obviously, each control structure must have only one input and one output
### Control Structures
#### Sequence
- The next instruction to be executed is the next instruction that appears in the program
#### Decision
- The next statement to execute depends on the outcome of the evaluation of a conditional expression
#### Repetition
- A statement is executed as long as a condition is met
#### Calls to a subprogram
- Calls to subprograms can also be considered as control structures since they alter the sequence of the control flow of the program
#### Other Control Structures
- Exception handling
	- an exception is an uncommon situation that causes action by the program
- Event handling
	- an event is a signal detected by the operating system that indicates an even has occurred that must be heeded
- Both mechanisms are worked in a similar way
- C++ provides for exception handling
- Python, C#, Java, and VB .Net provide for exception and event handling 
### Format of a C++ Program
```c++
<header-files>
<global-constants-declarations>
<global-variable-declaration>
<function-prototypes>

int main()
{
	<local-variable-declarations>
	<statements>
	return 0;
}

<function-definitions>
```
### Format of a Python Program
```python
# Note : Python is an intreted language
```
#### Compiled vs Interpreted 
- **Compiled Languages**
	- Compiled languages are converted directly into machine code that the processor can execute. As a result, they tend to be faster and more efficient to execute than interpreted languages. They also give the developer more control over hardware components, like memory management and CPU usage
- **Interpreted Languages
	- Run through the program line by line and execute each command

