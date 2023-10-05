

aliases: [ "20230928111153",  ]
tags: COMSC, COMSC335
date_created: 2023-09-28 11:11

# L08 - Context Free Grammar
---
## Simple Grammar
$A \rightarrow aX$
$A \in V$
$a \in T$
### Chomsky normal form
- All productions are in one of two forms
	- $A \rightarrow BC$
	- $A \rightarrow a$
### Greibach Normal Form
- Every Context Free Grammar in which $\lambda \in L(G)$ can be converted in Greiback normal form
- The process is not as clean as the conversion to Chomsky Normal Form
- Conversions are typically done through clever substitutions or a similar CNF approach
	- Example 6.9 - substitutions
	- Example 6.10 - create extra variables and productions
	- See supplemental material for detailed process
		- Posted on bridges later
	- ==One terminal on the left followed by any number of variables==
#### Example 6.9
- **Grammar must be normalized before this begins**
- Grammar:
	- $S \rightarrow AB$
	- $A \rightarrow aA|bB|b$
	- $B \rightarrow b$
		- This grammar has already been normalized

- Greiback normal form
	- $S \rightarrow aAB|bBB|bB$
	- $A \rightarrow aA|bB|b$
	- $B \rightarrow b$
#### Example 6.10
- Grammar must be normalized
- Grammar:
	- $S \rightarrow abSb|aa$
- Create two new productions
	- $A \rightarrow a$
	- $B \rightarrow b$
- Substitute these into original grammar
	- $S \rightarrow aBSB|aA$
	- $A \rightarrow a$
	- $B \rightarrow b$
>[! bug] If sub doesn't work
>Then things get complicated
## Membership approaches
### Brute Force
- Create each and every possible string paring down the list as infeasible strings are formed. Continue until all strings formed or w is found
### Length Based
- Create every string in some order such that short strings are formed first. If a string is formed > |w| then w is not in the language. 
	- Notice with CNF, and GNF every time a production is executed the string either stays the same length or increases. So it must either become |w| or longer in a <u>finite number of steps</u>
### Bottom up
- So far we've been building our strings from the 'top' down. We start at s and build from the beginning. Can we do the opposite
- ==Must be in Chomsky normal form==
	- We know where we want to be. Can we get there in one step? If so, then can we get there in two? and so on
	- Start at the bottom and see if we can find S
		- Based on creating all the substrings of w
			- Let $w=a_1a_2a_3...a_n$
			- Then the substring would be $w_{ij}=a_i...a_j$
			- Let $V_{ij} = (A \in V:A \Rightarrow ^*w_{ij})$
			- If $S \notin V_{ln}$ then $w \notin L(G)$ 

- We just need to figure out what all the $V_{ij}$ are
	- Compute V_{11}, V_{22}, V_{33} ... V_{nn}
		- These are just the terminals
	- $V_{1,2}, V_{2,3}, V_{3,4} ... V_{n-1,n}$
	- $V_{1,j}, V_{2,j+1}, V_{3,j+2} ... V_{nn}$
	- And so on until you reach w

- Its a bookkeeping nightmare
	- But this essentially a summation of unitions
#### Example
- $S \rightarrow AB$
- $A \rightarrow BB|a$
- $B \rightarrow AB|b$
	- This is in Chomsky normal form
	- Is $w = aabbb$ in L(G)?
