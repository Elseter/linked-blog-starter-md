---
aliases:
  - '"20230911153412"'
tags:
  - COMSC
  - COMSC230
date_created: 2023-09-11 15:34
Index: "[[COMSC.230 Index]]"
---

# COMSC.230 Lecture 2 - Grammar and Semantics
---
## Grammar and Semantics
### Todays Topics
- Grammar and parse tree examples
- Backus Naur Form (BNF) and parse tree definitions
- Constructing grammars
- Phrase structure and lexical structure
- Other grammar forms

#### Why is grammar important?
- Formally describes the structure of a programming language
- Helps us to understand the language (more insights)
- very useful for compiler and interpreter design

#### Syntax and Semantics
- Programming language **syntax**: how programs look, their form and structure
	- Syntax is defined using a king of formal grammar
	- ![[Screenshot 2023-09-11 at 3.38.46 PM.png]]
- Programming languages **semantics**: what programs do, their behavior and meaning/interpretation 
- On natural language, correct syntax may result may result in incorrect semantics
	- Need to make sure the computer interprets the syntax correctly (avoiding logical errors)

```c++
for(;;)
{
	std::cout << "check the H4x0rs @ COMSC230!";
}
```
	- Is this syntactically and semantically correct?

#### An English Grammar
- A sentence is a noun phrase, a verb, and a noun phrase
	- `<S> ::= <NP><V><NP>`
- A noun phrase is an article and a noun
	- `<NP> ::= <A><N>`
- A verb is 
	- `<V> ::= loves| jumps | eats`
- An article is 
	- `<A> ::= a | the`
- A noun is...
	- `<N> ::= fox | cat| human | fence`

- The grammar is a set of rules that say how to build a tree - a parse tree
- You put `<S>` at the root of the tree
- The grammar's rules dictate how the branches can be added at any point in the tree
- For instance, the rule
	- `<S> ::= <NP><V><NP>`
	- says you can add nodes `<NP><V>, and <NP>`, in that order, as children of `<S>`
- ![[Screenshot 2023-09-11 at 3.51.29 PM.png]]

### A Programming Language Grammar
![[Screenshot 2023-09-11 at 3.54.03 PM.png]]
- Based on the rules of this grammar
	- An expression can be constructed with the sum of two expression, or the product of two expressions, or a parenthesized subexpression
	- Or it can be one of the variables a, b, c
	- ![[Screenshot 2023-09-11 at 3.56.20 PM.png]]
- Which one of the following are valid expressions for this grammar:
	1. a
	2. a + b
	3. b + 4
	4. a + (b * c)

#### Some grammar Definitions
- Terminal Symbols - Base token of a programming language
	- Identifiers, numbers
	- Operators, restricted words
	- Make up the programming language

- Non-terminals - Representation of the structure (meta-language/ meta-syntax)
	- For English this may be a noun, verb, or article
	- For programming language this can be a subroutine, conditions, statement
	- Focus on syntax identification

#### Backus Naur Form Grammar
- Backus Naur Form (BNF) was created by:
	- John Backus, FORTRAN, IBM designer - ALGOL 58
	- Pater Naur, Danish computer scientist - Report ALGOL 60
- Other forms to express grammars:
	- Syntax Diagrams
	- Extended Backus Naur Form (EBNF)

### BNF Grammar Definition
- A BNF grammar consists of four parts:
	- The set of **tokens**
	- The set of **non-terminal** symbols
	- The start **symbol**
	- The set of **productions**
![[Screenshot 2023-09-11 at 4.03.46 PM.png]]

- The **tokens** are the smallest units of syntax
	- Strings of one or more characters of program text
	- They are atomic: not treated as being composed from smaller parts

- The **non-terminal** symbols stand for larger pieces of syntax
	- They are strings enclosed in angle brackets, as in `<NP>`
	- They are not strings that occur literally in program text
	- The grammar says how they can be expanded into strings of tokens

- The **start** symbol is the particular non-terminal that forms the root of any parse tree for the grammar

- The **Productions** are the tree-building rules
- Each one has a left-hand side, the separator ::=, and a right hand side
	- The **left-hand** side is a single **non-terminal**
	- The **right-hand** side is a sequence of one or more things, each of which can be either a **Token or non-terminal**
- A production gives one possible way of building a parse tree: it permits the non-terminal symbol on the left-hand side to have the things on the right-hand side, in order, as its children in a parse tree

#### Alternatives
- When there is more than one production with the same left-hand side, an abbreviated form can be used
- The BNF grammar can give the left-hand side, the operator ::= and then a list of possible right hand sides separated by the special symbol |
- `<exp>::= <exp> + <exp>| <exp> * <exp> | (<exp>)| a | b | c`
	- Note that there a six productions in this grammar

### Constructing grammars
- Visualize the tokes and branches (divide and conquer)
- Example: languages like C, C++, and Java declarations:
	- a type name, a list of variables separated by commas, and a semicolon
- Each variable can be followed by an initializer
	- int a;
	- boolean b,c
	- int a=1, b, c = false;

- Easy if we postpone defining the comma-seperated list of variables with initializers: 
	- `<var-dec> ::= <type-name><declarator-list>`
- primitive type names are easy enough too:
	- `<type-name> ::= boolean|byte|short|int|long|char|float|double`

- That leaves the comma separated list of variables with initializers
- Again, postpone defining variables with initializers, and just do the comma seperated list part:
	- `<declarator-list> ::= <declarator> | <declarator>, <declarator-list>`