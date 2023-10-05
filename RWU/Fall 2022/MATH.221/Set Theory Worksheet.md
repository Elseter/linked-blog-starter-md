
---
aliases: [ "20221107090143",  ]
tags: RWU, MATH.221, Math, Examples, DiscreteMath 
date_created: 2022-11-07 09:01
---
[[MATH.221 INDEX]]
# Set Theory Worksheet
---
## Main Document
[[Set Theory]]

### Examples from Set Theory - Worksheet 1

#### STW1 P.1
 $A =$ {$m \in \mathbb{Z}| m = 6r +12, \text { for } r \in \mathbb{Z}$}
	 $B =$ {$n \in \mathbb{Z} | n =3s \text { for } s \in \mathbb{Z}$}
**Prove**
	$A \subseteq B$ 
Work:
	$A =$ {$m \in \mathbb{Z}| m = 6r +12, \text { for } r \in \mathbb{Z}$} = {$..., -12, -6, 0, 6, 12, ...$}
	$B =$ {$n \in \mathbb{Z} | n =3s, \text { for } s \in \mathbb{Z}$} = {$..., -6, -3, 0, 3, 6, ...$}
>[!example] **Proof**
>Suppose $x \in A$. Then $x = 6r+12$ for some $r \in \mathbb{Z}$ 
>Then $x = 3(2r+4)$. Where $2r+4 \in \mathbb{Z}$. Then $x = 3(\mathbb{Z})$
>$\therefore x \in B$
>$\therefore A \subseteq B$

##### STW1 P.1.2
 $A =$ {$m \in \mathbb{Z}| m = 6r +12, \text { for } r \in \mathbb{Z}$}
	 $B =$ {$n \in \mathbb{Z} | n =3s \text { for } s \in \mathbb{Z}$}
**True or False**
	$B \subseteq A$
Work:
	$B \subseteq A \Leftrightarrow \forall x. x \in B \Rightarrow x \in A$
	$B \nsubseteq A \Leftrightarrow \exists x, x\in B \text{ and } x \notin A$ 
>[!example] Proof by CounterExample
>$3 \in B \text{ and } 3 \notin A$
>
>**Justification for B**
>	$3 = 3 \cdot 1$
>	
>**Justification for A**
>	Assume $3 \in A$
>	Then, $3 = 6r + 12 \text{ for some } r \in \mathbb{Z}$
>	This means, $r = \frac{-9}{6} = \frac{-3}{2}$
>	This is a contradiction $\Box$
>$\therefore B \nsubseteq A$

##### STW1 P.1.3
 $A =$ {$m \in \mathbb{Z}| m = 6r +12, \text { for } r \in \mathbb{Z}$}
	 $B =$ {$n \in \mathbb{Z} | n =3s \text { for } s \in \mathbb{Z}$}
**True or False**
$A \subset B$
>[!example] Proof
>From part STW1 P.1 (a), $A \subseteq B$
>From part STW1 P.1.2 (b), $3 \in B \text{ and } 3 \notin A$

#### STW1 P.4
$R =$ {$x \in \mathbb{Z}: 2|x$}
$S =$ {$y \in \mathbb{Z}: 3|y$}
$T =$ {$x \in \mathbb{Z}: 6|x$}

##### A.) $R \subseteq T$
CounterExample:
	$2 \in R \text{ and } 2 \notin T$
	
##### B.) $T \subseteq R$
>[!example] Proof:
Suppose $x \in T$ , $x = 6k \text{ for some } k \in \mathbb{Z}$
Now, $x = 2(3k)$
$\therefore T \subseteq R \space \Box$
##### C.) $T \subset S$
>[!example] Proof:
>We need to prove $T \subset S$ and, $x \in S \text{ and } x \notin T$
>
#### STW1 P.5
$A =$ {$m \in \mathbb{Z}| m = 6r - 5, \text { for } r \in \mathbb{Z}$}
$B =$ {$n \in \mathbb{Z} | n =3s + 1 \text { for } s \in \mathbb{Z}$}

##### A.) $A \subseteq B$
>[!example] Proof
Suppose, $x \in A$
Then, $x = 6r - 5 \text{ for some } r \in \mathbb{Z}$
Now, $x = 6r -5$ = ($\text{unknown} = 3\mathbb{Z} +1$)
**Set Equal to one another**
$6r - 5 = 3s + 1$
$6r - 6 = 3s$
$2r - 2 = s$
** Plug in**
$x = 6r - 5$
$x = 3(2r-2) +1$
> $\therefore x \in B \text{ and } A \subseteq B \Box$
True

##### B.) $B \subseteq A$
**Set Definitions**
	$B \subseteq A \Leftrightarrow \forall x. x \in B \Rightarrow x \in A$
	$B \nsubseteq A \Leftrightarrow \exists x, x\in B \text{ and } x \notin A$ 
>[!example] CounterExample
>$-2 \in B \text{ and } -2 \notin A$
>
>**Proof of: **$-2 \in B$
>$-2 = 3s + 1$
>$-3 = 3s$
>$s = -1$
>
>**Proof of: **$-2 \notin A$
>$-2 = 6r - 5$
>$3 = 6r$
>$r = \frac{3}{6} = \frac{1}{2} \notin \mathbb{Z}$
>This is a contradiction $\Box$


### Set Size Examples

#### 1.)
If A = {1, 2}, B= {4, 5, 6} then compute
##### A.) $|AxB|$
		$6 = |A| \cdot |B|$
##### B.) $|\mathscr{P}(B)|$
$\mathscr{P}(A)$ = {$\varnothing$, {1}, {2}, {1, 2}}
= 4
##### C.) $|\mathscr{P}(AxB)|$
= $2^6 = 64$
##### D.) $|\mathscr{P}(B)|$
$\mathscr{P}(B)$ = {$\varnothing$, {4}, {5}, {6}, {4, 5}, {5, 6}, {4, 6}, {4, 5, 6}} 
= 8
### Set Algebraic Properties Worksheet
#### 2.)
##### B.) $(A \backslash C) \cup (B \backslash C) = (A \cup B) \backslash C$
>[!example] Proof: By Algebra
>L.S = $(A \backslash C) \cup (B \backslash C)$
>L.S = $(A \cap C^c) \cup (B \cap C^c)$
>L.S =$C^c \cap (A \cup B)$
>L.S = $(A \cup B) \backslash C$
>L.S = R.S
>$\therefore (A \backslash C) \cup (B \backslash C) = (A \cup B) \backslash C$

##### D.) $A \backslash (A \cap B) = A \backslash B$
![[MATH.221 A set minus B.png|200]]
>[!example] Proof: (Method 1 : by Algerbra)
>L.S = $A \backslash (A \cap B)$
>L.S = $A \cap (A \cap B)^c$ 
>- See Tip
>L.S = $A \cap (A^c \cup B^c)$
>L.S = $(A \cap A^c) \cup (A \cap B^c)$
>L.S = $\varnothing \cup (A \cap B^c)$
>L.S = $A \cap B^c$
>- See Reverse Tip
>L.S = $A \backslash B$
>L.S = R.S

>[!note] Tip
>$$X \backslash Y = X \cap Y^c$$
>Set minus is the same thing as **Union with the compliment**

>[!example] Proof: (Method 2 : Element Argument)
>To Prove $(A \backslash (A \cap B)) \subseteq (A \backslash B)$
>Suppose,  $x \in A \backslash (A \cap B)$
>This means, $x \in A \text{ and } x \notin A \cap B$
>This implies, $x \in A \text{ and }  \text{ not } x \in A \cap B$
>Consequently, $x \in A \text{ and }  \text{ not } (x \in A \text{ and } x \in B)$
>This results, $x \in A \text{ and } x \notin A \text{ or } x \notin B$
>Now, $(x \in A \text{ and } x \notin A) \text{ or } (x \in A \text{ and } x \notin B)$ 
>This implies, $x \in A \text{ and } x \notin B$
>$\therefore x \in A \backslash B$
>This gives $(A \backslash (A \cap B)) \subseteq (A \backslash B)$

>[!example] Proof: (Method 2: Element Argument Reverse Argument)
>Now suppose $x \in A \backslash B$
>Then, $x \in A \text{ and } x \notin B$
>Now, $x \in A \text{ and } x \notin A \cap B$
>This provides, $x \in A \backslash (A \cap B)$
>This means, $$(A \backslash B) \subseteq (A \backslash(A \cap B))$$
>$\therefore (A \backslash B) = (A \backslash(A \cap B))$
>$\Box$








