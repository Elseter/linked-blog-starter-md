
---
aliases: [ "20221130091008",  ]
tags: RWU, MATH.221, DiscreteMath, Math
date_created: 2022-11-30 09:10
---
[[MATH.221 INDEX]]
# Relations
---
#### Additional Info
- Found in Chapter 8 of the textbook
- [[MATH.221 Relations - Part 1.pdf]]

## General
- We want to relate two symbols and understand the relation
- Can Symbols with different appearances have equivalent value?
- $5 = \mathbb{5}$?

### Definition of a Relation
>[!definition] A *Relation* (R) from set A to set B, is a subset of AxB
>A is the **Domain**
>B is the **Co-Domain**

>[! example] Example #1:
>		- Let A = {1, 2, 3}
>		- Let B = {a, b}
>		- Then R = {(1, a), (2, b), (3, b)}
>		- This is a Relation from A to B

>[! Definition] Notation 
>If $(x,y) \in R$ where $R$ is a relation, we indicate it by $xRy$
>This is read as $x$ is Related to $y$ under $R$

## Types of Relations

>[! definition] 
>Let A be a non-empty set and R be a relation on A
>1. R is <u>reflexive</u> if $$ \forall x \in A, xRx$$
>2. R is <u>symmetric</u> if $$ \forall x,y \in A, xRy \Rightarrow yRx$$
>3. R is <u>transitive</u> if $$ \forall x,y,z \in A, xRy \text{ and } yRz \Rightarrow xRz$$
- If R satisfies all these properties, then R is called an <u>equivalence relation</u>

### Equivalence Classes
>[!definition] Notation
>$[x] :=$ equivalence class of x
>f
>For Example:
>$[0]$ = {$x \in \mathbb{Z} \space|\space xS0$}
>      = {$x \in \mathbb{Z} \space|\space x - 0 = 7k \text{ for some } k \in \mathbb{Z}$}

### Worksheet Examples 

#### Q1.RP1
>[! Info] Provided Info
>$A =${$1, 2, 3$}, $B =$ {$7, 9$}

##### A.) Write down 3 different relations from A to B
>[!Done]
>$R =$ {} : the empty relation
>$S =$ {$(1, 7)$}
>$T =$ {$(1, 7), (2, 9), (3, 7)$}

##### C.) Write down three different Relations from B to A
>[!Done]
>$R =$ {} : the empty relation
>$S =$ {$(7, 1)$}
>$T =$ {$(7, 1), (9, 2)$}

#### Q2.RP1
>[!Info] Provided Info
>Let $L$ be a relation from $\mathbb{R}$ to $\mathbb{R}$ given by $$ \forall (x, y) \in \mathbb{R}x\mathbb{R} \text{, } xLy \Leftrightarrow \text{ x is less than y}$$

| question  | True or False | Compare |
| --------- | ------------- | ------- |
| $5L8$     | True          | 5 < 8     |
| $6L2$     | False         |  6 < 2       |
| $(-5)L10$ | True          |     -5 < 10    |
| $3L3$     | False         |   3 < 3      |

#### Q3.RP1
>[! Info] Provided Info
>Let $A =$ {$3, 4, 5, 6, 7, 8, 9$} and define the relation $R$ on $A$ by $$ \forall x,y \in A \text{, } xRy \Leftrightarrow 2|(x-y)$$

##### A.) Write down all elements that are related to 3
- In other words, find x such that xR3 = x-3 is even
- All such elements:
		3, 5, 7, 9

##### B.) Write down all elements that are related to 7
- In other words, find x such that xR7 = x - 7 is even
- All such elements:
		3, 5, 7, 9

##### C.) "Directed Graph" illustration
![[MATH.221 Relations drawing.png]]
- Additionally, each of these points also loops back upon itself
- Should be a line between 9 and 5 going in both directions
	- Just an error on my part for not including it
###### Operations
- Observations about the graph above
>[! done] Observations
>1. Two Patricians of Set A **(odd / even)**
>2. Each arrow goes in both directions **(symmetric)**
>3. Triangular patterns **(Transitive)**
>4. Loops around every element **(Reflexive)**

#### Q5.RP1
>[! Info] Provided Info
>Let $A =$ {$3, 4, 5, 6, 7, 8, 9$} and define the relation $R$ on $A$ by $$ \forall x,y \in A \text{, } xRy \Leftrightarrow x|y $$

##### C.) Draw a Directed Graph
![[MATH.221 Relations drawing2.png]]
- Each element is **reflexive** as they will divide themselves
- Not Symmetric
- Not Transitive

#### Professor Provided Example
>[! info] Provided Info
>Let S be a relation defined on $\mathbb{Z}$ by: $$\forall x,y \in \mathbb{Z},\space xSy \Rightarrow 7|(x-y)$$

##### A.) Show that S is an equivalence relation
- Go through each property
###### Reflexive
>[! done] Proof of Reflexivity
>Let $x \in \mathbb{Z}$
>Then, $x-x = 0 = 7 \cdot 0$
>This means, $7|(x-x)$
>$\therefore xSx$

###### Symmetric
>[! done] Proof of Symmetry
>Let $x,y \in \mathbb{Z}$
>Suppose, $xSy$
>Then, $x-y = 7k \text{ for some } k \in \mathbb{Z}$
>Then, $y-x = 7(-k)$
>Which equals, $y-x = 7k$
>$\therefore xSy \Rightarrow ySx$

###### Transitive
>[! done] Proof of Transitive Property
>Let $x, y, z \in \mathbb{Z}$
>Suppose $xRy \text{ and } yRz$
>Then, $x-y = 7k \text{ for some } k \in \mathbb{Z}$
>and, $y-z = 7l \text{ for some } l  \in \mathbb{Z}$
>Then, $x-z = 7k + 7l$
>Which also equals, $x-z = 7(k+l)$
>$\therefore xSy \text{ and } ySz \Rightarrow xSz$

##### B.) Write down all '<u>equivalence classes</u>'
>[!done] Examples
>$[0]$ = {$x \in \mathbb{Z} \space|\space xS0$}
>      = {$x \in \mathbb{Z} \space|\space x - 0 = 7k \text{ for some } k \in \mathbb{Z}$}
>      {$..., -14, -7, 0, 7, 14, ...$}
>
>$[1]$ = {$x \in \mathbb{Z} \space|\space xS1$}
>= {$x \in \mathbb{Z} \space|\space x - 1 = 7k \text{ for some } k \in \mathbb{Z}$}
>$x = 7k +1$
>{$..., -13, -6, 1, 8, 15, ...$}
>
>$[2]$ = {$..., -12, -5, 2, 9, 16, ...$}
>$[3]$ = {$..., -11, -4, 3, 10, 17, ...$}
>$[4]$ = {$..., -10, -3, 4, 11, 18, ...$}
>$[5]$ = {$..., -9, -2, 5, 12, 19, ...$}
>$[6]$ = {$..., -8, -1, 6, 13, 20, ...$}
>$[7]$ = {$..., -7, 0, 7, 14, 21, ...$}
>- $[7]$ is the same class as $[0]$, meaning we have looped
>- There are 7 sets of equivalences classes

![[MATH.221 Relation drawning3.png]]
>[!note]
>Let R be an equivalence relation on A. Then, the collection of equivalence classes of R has the following properties:
>
>$(I)\space\space [a] = [b] \Leftrightarrow aRb$
>-  In previous computation $[1] = [8]$
>
>$(II) \space\space [a] \cap [b] \neq \varnothing \Leftrightarrow [a] = [b]$
>$(II)$ If the collection of equivalence classes indicated by 
>$C =$ {$[a_1], [a_2], [a_3],... [a_n], ...$}
>- Then, $A = [a_1] \cup [a_2] \cup [a_3] \cup [a_4] \cup ... \cup [a_n] \cup...$
### See Eq Relations and Classes for more info
[[Equivalence Relations and Classes]]
