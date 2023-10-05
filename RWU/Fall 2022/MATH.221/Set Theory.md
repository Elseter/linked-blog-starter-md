
---
aliases: [ "20221104090232",  ]
tags: RWU, MATH.221, Math, DiscreteMath 
---
[[MATH.221 INDEX]]
# Set Theory
---
## Set Theory (Ch. 6)
**Definition:** A set is a <u>well-defined</u> collection of <u>objects</u>
### Set Operations/Definitions
Let A, B be sets

#### Intersection
1. $A \cap B =$ A <u>intersection</u> B
	 $A \cap B =$ {$x | x \in A,\text{ and } x \in B$}
		*x exists such that x is in A <u>and</u> B*
![[MATH.221 set intersection.jpg]]

#### Union
2. $A \cup B =$ A <u>union</u> B
	 $A \cup B$ = { $x|x \in A \text{ or } x \in B$ }
		*x exists such that x is in A <u>or</u> B*
![[MATH.221 Set Union.jpg]]
#### Subset
3. $A \subseteq B$ : A is a <u>subset</u> of B 
	  $A \subseteq B \Leftrightarrow \forall x, x \in A \Rightarrow x \in B$  
		 This includes the possibility of A = B
![[MATH.221 Set Subset.jpg]]
#### Proper Subset
4. $A \subset B$ : A is a <u>proper subset</u> of B
	  $A \subseteq B \Leftrightarrow \forall x, x \in A \Rightarrow x \in B$  **and** $\exists y \in B, \text{ such that } y \notin A$ 
			This means $A \neq B$ 

#### Set Equality
5. $A = B$ : Set equality
		$A = B \Leftrightarrow A \subseteq B \text { and } B\subseteq A$ 

#### Not Subset
6. $A \nsubseteq B \Leftrightarrow \text { not } (A \subseteq B)$
		$\Leftrightarrow \text {not}(\forall x, x \in A \Rightarrow x \in B)$

#### Compliment
7. $A^c$ := The <u>compliment</u>of A
		$A^c =$ {$x \in \mathbb{U} | x \notin A$}
		x is in the universal set, but not in A

#### Set Minus (Relative Compliment)
8. $A\setminus B$ : A (set) minus B
		: <u>Relative Compliment</u>
		$A \setminus B$ := {$x | x \in A \text { and } x \notin B$}

#### Cartesian Product
9. $AxB$ : <u>Cartesian Product</u> (set product)
		$A x B$ := {$(a,b) | a \in A \text{ and } b \in B$}
		I.E 
		A = {a, b, c}
		B = {1, 2}
		AxB = {(a,1), (b,1), (c,1), (a,2), (b,2), (c,2)}

#### Power Set
10. $\mathscr{P}(A)$ : <u>Power set</u> of A
		$\mathscr{P}(A)$ := {$X | X \subseteq A$}
		   := The collection of all subsets of A
		I.E
		A = {1, 2}
		$\mathscr{P} (A)$ = { {}, {1}, {2}, {1, 2} }

#### Empty Set
11. <u>The Empty Set</u> : {}, $\varnothing$
		$\varnothing =$ A set with no elements

### Set Size
- Notation:
	- The size of set A is denoted by |A|
Examples
1. If A = {4, 5, 6}
		$|A| = 3$
1. $|\mathbb{N}| = |\mathbb{Z}| = |\mathbb{Q}|$
		Countable Infinity

#### Definition
If A is finite, then |A| is just the count of elements in A
>[!Note] Shortcut
>For any set $|\mathscr{P}(A)| = 2^{|A|}$

>[!Note] Shortcut
>For A, B sets $|AxB| = |A| \cdot |B|$


## See Examples
[[Set Theory Worksheet]]

