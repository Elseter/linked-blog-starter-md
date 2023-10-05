
---
aliases: [ "20230912110349",  ]
tags: COMSC, COMSC.335
date_created: 2023-09-12 11:03
---
# L04 Finite Automata and Regular Languages
---
## Going from Expression to NFA
- One state to another
	- ==Primitive==
- One state to another to another
	- ==Concatenation==

### Pay attention to parenthesis and Exponents
- $(a \cup ab)*$
- $((a)(ab))*$

- These two languages look very similar
- aabaabaabaab
	- would be accepted by both
- ababababab
	- Would only be accepted by the first

- Going from RE to NFA proves every regular expression can be defined by regular language
- But does every regular language have a RE
	- Does every NFA lead to a RE?

### Build one
- Regular Expression:
	- $(a+b)^*abb(abb)^*a$
	- Can we turn that expression into an NFA
	- ![[Screenshot 2023-09-12 at 11.18.02 AM.png]]

### Going from NFA to expression (ONLY WORKS WITH 1 FINAL STATE)
- For every pair on nodes j and k (where j may equal k)
	- if there are arrows from j to k with labels
		- $l_{j,k}^1, l_{j,k}^2, l_{j,k}^3, ... l_{j,k}^m$
	- then replace with a single arrow
		- $l_{j,k}^1 \cup l_{j,k}^2 \cup l_{j,k}^3 \cup ... l_{j,k}^m$
	- for every i -2, 3, 4, ... , n-1 do
		- for every pair of nodes j and k (where j may equal k) such that there is an arrow from j to i and there is an arrow from i to k do 
		1. if there is no arrow from i to i
			- then add an arrow from j to k labeled 
		2. if there is an arrow from i to i 
			-  then add an arrow from j to k labeled 

## Grammars
- A grammar G = (V, T, S, P)
	- V set of NonTerminals (variables)
	- T set of Terminals 
	- P set of Propagations
	- S starting symbol (an element of V)

- The language L(G) = {$w|w \in \sum^* , S \Rightarrow ^{*}w$}
	- All terminal strings derivable from the starting symbol
	- **A Grammar can only generate strings from its language**

### Right-Linear Grammar
- G = (V, T, S, P)
	- $A \rightarrow xB$
	- $A \rightarrow x$
		- $A, B \in V$
		- $x \in T^*$
- One variable per production and it must be rightmost

- $A \rightarrow abbA | aA | bB$
- $A \rightarrow b$
- $B \rightarrow bB | b$

#### Generate Regular Languages
- Right-linear grammars generate Regular languages
- Think of Variables as verticies
- Think of T as inputs
- Productions are transitions

- Regular Languages have Right-linear grammars
	- Think of states as Variables
	- Think of $\sum$ as Terminals
	- Think of $\delta$ as Productions

>[! note] Exchangeable
>Right Linear grammars can be converted to Regular languages which can be converted to regular expressions which can be converted to NFAs which can be converted to an DFA
### Left-Linear Grammar
- G = (V, T, S, P)
	- $A \rightarrow Bx$
	- $A \rightarrow x$

- Left-linear grammars are Right-linear grammars in disguise
	- Reverse the position of B
		- $Bx$ becomes $xB$
		- Reverse the terminal string
		- $A \rightarrow x^RB$
		- $A \rightarrow x^R$
### Linear Grammar
- at most one variable per production
- G = ({A,B,S}, {a, b} )
