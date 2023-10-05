

aliases: [ "20230926110604",  ]
tags: COMSC, COMSC335
date_created: 2023-09-26 11:06

# L08 - Context Free Grammars
---
## Context Free Grammars
- Only one variable on the left side of the grammar
### Substitution
- Productions of the form
- $A \rightarrow x_1Bx_2$
- $B \rightarrow y_1|y_2|y_3|... y_n$
	- substitute B for everywhere B appears in another production
	- Can not work if A = B
	- $A \rightarrow x_1y_1x_2 | x_1y_2x_2 | x_1y_3x_2 ...$
### Remove $\lambda$
- A production may be $\lambda$ even if the language does not accept the empty string
- $S \rightarrow aAb|bBa$
- $A \rightarrow aAb | \lambda$
### Remove Unit Productions
- A unit production has the form $A \rightarrow B$
	- $S \rightarrow Aa | B$
	- $B \rightarrow A|bb$
	- $A \rightarrow a |bc| B$
- Original non-unit
	- $S \rightarrow Aa$
	- $B \rightarrow bb$
	- $A \rightarrow a |bc$

- New non-unit productions
	- $S \rightarrow Aa$
	- $B \rightarrow bb$
	- $A \rightarrow a |bc$
### Remove Useless Productions
- A production is useless if it can not be transformed into a terminal string
- Additionally, a production is useless if it can not be reached from the Start state (S)
	- Any variable that is on the left hand side that does not appear on the right hand side can simply be disregarded
## Order is Important
1. Remove Lambda production
2. Remove unit-productions
3. Remove useless productions (1, then 2)
	1. A significant number of errors come from not doing these in the proper order
	2. This results in a normalized grammar
>[! bug] IMPORTANT
>Follow the order listed above, otherwise you will end up with an invalid solution

## Chomsky Normal Form
- All productions are in one of two forms:
	- $A \rightarrow BC$
	- $A \rightarrow a$
		- Variable goes to two variables
		- variable goes to single terminal
		- $A,B,C \in V; a \in T; \lambda \in L(G)$
### Nice thing about Chomsky
- Every context free grammar in which $\lambda \in L(G)$ can be converted to Chomsky normal form
- **Step 1:**
	- Create $G_1 = (V_1, T, S, P_1)$ from G
		- ==Ensure G has been normalized==
	- If productions are already in the form $A \rightarrow BC$ or $A \rightarrow x$ keep it
	- Consider productions of the form 
		- $A \rightarrow z_1x_2x_3x_4...x_n$ where $x_i \in (V\cup T)$
	- Create variable $B_a$ and production $B_a \rightarrow a$ for each $a \in T$
		- Let $C_i = x_i$ if $x_i \in V$
		- Let $C_i = B_a$ if $x_i=a$
	- $A \rightarrow z_1x_2x_3x_4...x_n$ becomes
		- Add $A \rightarrow C_1C_2C_3C_4...C_n$ to $P_1$
		- Add $B_a \rightarrow a$ to $P_1$ for each $B_a$
- **Step 2:**
	- $A \rightarrow C_1C_2C_3C_4...C_n$ has too many variables
		- We can only have two variables on the right hand side of any production
		- Create variables $D_1, D_2, D_3, D_{n-2}$
	- Deconstruct A as follows
		- $A \rightarrow C_1D_1$
		- $D_1 \rightarrow C_2D_2$
		- $D_2 \rightarrow C_3D_3$
		- ...
		- $D_{n-2} \rightarrow C_{n-1}C_n$
			- Each production in $P_1$ is in CNF
- Organize, all variables first, then terminals second
- Don't re-create variables that already exists... duh