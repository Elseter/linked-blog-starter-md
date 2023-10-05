---
aliases:
  - '"20230906154139"'
tags:
  - COMSC
  - COMSC230
date_created: 2023-09-06 15:41
Index: "[[COMSC.230 Index]]"
---

# COMSC.230 Lecture 1
---
## Todays Topics
- Programming Language Levels of Abstractions
- Assembly Language (Briefly)
- Logical operators
- Multiple Programming paradigm
- History of Programming
- Programming Cycle and terms definitions

#### Knowledge Check
- The lowest representation of information on Hardware?
	- Electrical voltage (energy states)
- What is an Opcode?
	- Portion of a machine_language instruction that specifies the operation to be performed and the data registers they will process

### Many Connections
- Programming languages touch upon virtually all areas of computer science and multiple levels of abstraction: 
	- from mathematical theory of **Formal Languages** and **Automata** to the implementation of **Operating Systems**

	- Levels of abstraction
		- Hardware -  (voltage level)
		- Machine language  - (Opcode, Qbits)
		- Assembly language  - (X86)
		- Medium level language - (C)
		- High-Level language - (C++, Python)
		- Human Language - Alexa, Siri

#### Hardware Level
- The bit is the most basic unit of information in computing and digital communications
	- The bit represents a logical state with one of two possible values
- These values are most commonly represented as either "1" or "0", but other representations such as true/false, yes/no, on/off, or +/- are also commonly used
#### Machine Code
- Machine code is the only language a computer can process directly without a previous transformation
- True machine code is a stream of raw data
	- The data is represented digitally in a binary octal or in hexadecimal format
- The programmers use high level languages to avoid the complexity tied to machine code and memorizing architectures
#### Assembly Language
- Generates an executable code by translating combinations of *mnemonics* and *syntax* for operations and addressing modes into their numerical equivalents

### Logical Operations
#### and
| Bit 1 | Bit 2 | Bit3 |
|:-----:|:-----:|:----:|
|   0   |   0   |  0   |
|   0   |   1   |  0   |
|   1   |   0   |  0   |
|   1   |   1   |  1   |
- The format of these instructions are 
	- and destination, source
- Symbol: &&
#### or
| Bit 1 | Bit 2 | Bit 3 |
|:-----:|:-----:|:-----:|
|   0   |   0   |   0   |
|   0   |   1   |   1   |
|   1   |   0   |   1   |
|   1   |   1   |   1   |
- The format of these instructions are:
	- or destination, source
- Symbol: ||

### Multiple programming paradigms
#### Procedural 
- Highlights of Procedural/Imperative languages
	- Variable assignment
	- Relies on Iteration
```c
int fact(int n){
	int result = 1;
	while (n>0)
		result *= n--;
	return result;
}
```
##### Number Data Types
- Byte
	- 8-bit signed
- Short
	- 16-bit signed
- int 
	- 32-bit signed
- long 
	- 64-bit signed
- float
	- 32-bit IEEE 754
- double
	- 64-bit IEEE 754

#### Functional 
- Highlights of functional languages (e.g. Lisp, Haskell, Scheme)
	- Heavy use of Recursion
	- Single value variables
```lisp
defun fact (n)
	(if (= n 0) 1
	)
```
#### Logical 
- Highlights of Logical Languages (e.g. Prolog, Alice)
	- Consist of rules that specify the program solution

#### Object-Oriented
- Highlights of Functional OO languages (e.g. Java, Python, C++)
	- Objects with allowed operations
	- Object Memberships

### History of Programming Languages
#### Babylon
- Babylon was in modern day Iraq
- Cuneiform writing was used in Babylon, founded by Hammurabi around 1790 BC
- Many Babylonian clay tablets survive to today
	- No concept of variables
	- Instead numbers serve as a running example
#### Bagdad
- Near ancient Babylon and founded around 762
- A great center of scholarship, art and poetry
- 780-850: Mohammed Al-Khorexmi
	- Also known by the latin form of his name, Algoritmi was a Muslim court mathematician, astronomer and geographer

#### Euclid's Algorithm
- Computing the greatest common divisor (GCD), given two positive a and b such that a > b

### Programming cycle
- ANALYZE the problem and SPECIFY what the solution must do
	- requirments identification and definition
- Develop a GENERAL SOLUTION (ALGORITHM) to solve the problem