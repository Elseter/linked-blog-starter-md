
---
aliases: [ "20221024090253",  ]
tags: RWU, MATH.221, Math, DiscreteMath 
date_created: 2022-10-24 09:02
---
[[MATH.221 INDEX]]
# Mathematical Induction
---
[[MATH.221 Mathematical Introduction-Part 1.pdf|Mathematical Introduction-Part 1 Worksheet]]

## Introduction
- This is chapter 5 in the textbook

Purpose: To prove $\forall n \in \mathbb{N} \cup \{0\}, P(n) \text{ is true}.$
Method. If, 
1. $P(0)$ is true.
2. $\forall k \in \mathbb{N} \cup {0} P(k) \text{ is true} \implies P(k+1) \text{ is true}$
3. Then $\forall n \in \mathbb{N} \cup \{0\}, P(n) \text{ is true}.$

## Initial Examples
### Example 1
**Prove:** $$\forall n \in \mathbb{N}, 1+2+3+...+n = \frac{n(n+1)}{2}$$
### Example 2
Prove: When n is an <u>integer</u> such that $$n \gt 2, n^2 \lt 2^n$$
### Example 3
$a_n = n^2 - n +1$ for $n \le 1$ give the first 3 examples **(This is an Explicit Definition)**

$a_1 = 1^2 -1 + 1 = 1$
$a_2 = 2^2 -2 + 1 = 3$
$a_3 = 3^2 -3 + 1 = 7$

### Example 4
**This is an ==Inductive== Example**
$C_n+1 = 2c_n +1$
with $c_1 = 3$

$c_2 = 2c_1 + 1$
$c_3 = 2c_2 + 1$
$c_4 = 2c_3 + 1$

## Summation notation
**Sigma Notation** $$\sum_{i=1} ^{5} i(i+1)$$
- i = 1 is our starting (initial) value
- 5 is out terminal value
- i(i+1) is the function these values will be plugged into

**Sigma Notation Expanded**
$1(1+1) + 2(2+1) + 3(3+1) +4(4+1) +5(5+1)$

**Example**
$$\sum_{k=1} ^{n} k = \frac{n(n+1)}{2}$$
- This is the same as the first problem example from above, but written in a different form

### Practice Problems from worksheet
- Write the following problem in sigma notation
2b.) $-1^2 + 2^2 -3^2 + 4^2 +(-1)^n(n^2)$ $$\sum_{i=1} ^{n} (-1)^i(i^2)$$
- Expand the following notation
3a.) $\sum_{k=1} ^{5} k2^k$ $$1(2)^1 + 2(2)^2 + 3(2)^3 + 4(2)^4 + 5(2)^5$$
## Mathematical Induction
### MIP1 4
**Notations:
		LHS = Left Hand Side
		RHS = Right Hand Side**

Prove: $$\forall n \in \mathbb{N}, 1+2+3+...+n = \frac{n(n+1)}{2}$$Proof:
- Step 1: Proof for initial value, $n=1$
		*When* $n=1$,
			*L.H.S = 1*
			*R.H.S* = $\frac{1(1+1)}{2} = 1$
			*L.H.S = R.H.S*
			When $n=1$, the result holds

- Step 2: Assume the result is true for $n=k\;for\;some\;k \in \mathbb{N}$
		*This means,* $1+2+3+...+k = \frac{k(k+1)}{2}$

- Step 3: Now, based on step 2, prove the statement holds for $n=k+1$
	*Proof:*
		LHS = $1+2+3+...+k+(k+1)$
			= $\frac{k(k+1)}{2} + (k+1)$
			= $(k+1)(\frac{k+2}{2})$
		RHS = $\frac{(k+1)(k+2)}{2}$

### MIP1 5 Sums
**Prove:**
$\forall n \in \mathbb{N}, 1^2 + 2^2 + 3^2 +... + n^2 = \frac {n(n+1)(2n+1)}{6}$
$\sum_{k=1}^{n} k^2 = \frac{n(n+1)(2n+1)}{6}$

Proof
>When $n=1$
>L.H.S = $1^2 = 1$
>R.H.S = $\frac{1(1+1)(2(1)+1)}{6} = \frac{6}{6} = 1$ 
>$\therefore \text { When } n=1 \text{, the result holds}$ 
>Assume the result for $n=k \text{ where } k \in \mathbb {N}$ 
>$1^2+2^2+3^2+... k^2 = \frac{k(k+1)(2k+1)}{6}$              **-(1)**
>Now consider the case of $n = k+1$ 
>L.S = $1^2+2^2+3^2+...k^2+(k+1)^2$
>L.S = $\frac{k(k+1)(2k+1)}{6} + (k+1)^2$                     **- by (1)**
>L.S = $\frac{(k+1)}{6}\left[k(2k+1) + 6(k+1)\right]$
>L.S = $\frac{(k+1)}{6}\left[2k^2+7k+6\right]$
>L.S = $\frac{(k+1)((k+1)+1)(2(k+1)+1)}{6}$ = R.S $\Box$

>R.S = $\frac{(k+1)(k+2)(2K+2)}{6}$

### MIP1 7
**Prove:** 
$\forall n \geq 0,6 \space |\space (7^n -1)$

Proof: 
>**Base Case: \[**
>When $n=0$
>$7^0 - 1 = 0 = 6 \cdot 0$
>$\therefore$ The result golds
>**]**
>
> **Induction Hypothesis: \[**
> Assume that the result for $n=k \text{ where } k \geq 0$.
> Then $6\space |\space (7^k-1)$
> $(7^k -1) = 6 \cdot l \text { for some } l \in \mathbb{Z}$ 
> $7^k = 6l +1$
> **]**
> 
> **Induction: \[**
> Now consider $n=k+1$
> Then $(7^{k+1} -1) = 7^k \cdot 7 -1$
> $(6l+1) \cdot 7 -1$
> $42l + 7 -1 = 42l + 6$
> $6(7l + 1)$ where $7l +1 \in \mathbb{Z}$
> $\therefore$  The result holds $\Box$

### MIP1 8
**Prove:**
$\forall n \geq 0,\space 6 \space |\space (n^3 -n)$

>**Base Case: \[**
>When $n=0$
>$n^0 - n = 0 = 6 \cdot 0$
>$\therefore$ The result holds
>**]**
>
> **Induction Hypothesis: \[**
> Assume that the result for $n=k \text{ where } k \geq 0$.
> Then $6\space |\space (n^3-n)$
> $(k^3 -k) = 6 \cdot l \text { for some } l \in \mathbb{Z}$ 
> $k^3 = 6l +k$
> **]**
> 
> **Induction: \[**
> Now consider $n=k+1$
> Then $((k+1)^3 - (k+1)) = k^3 + 3k^2 +2k$
> $(6l +k) + 3k^2+2k = 6l+3k^2+3k$
> $6(l) + 3k(k+1)$
> k(k+1) is the product of two consecutive integers, which is always even
> $6(l) + 3(2 \cdot m) \text { where } m \in \mathbb{Z}$ 
> $6(l+m)$
> $\therefore$  The result holds $\Box$

### MIP2 7 Multi-Step Induction
**Given:**
$a_0 = 5, a_1 = 16$
$a_{k+2} = 7a_{k+1} - 10a_{k}$ 
**Need to Prove**:
$a_n = 3 \cdot 2^n + 2 \cdot 5^n \text{ for all } (n \geq 0)$

**Proof:**
>When $n=0$
>	$a_0 = 3 \cdot 2^0 + 2 \cdot 5^0 = 3+2 = 5$
>When $n=1$
>	$a_1 = 3 \cdot 2^1 + 2 \cdot 5^1 = 6+10 = 16$
>Assume that the result holds for $n=k$ and $n=k+1$ with $k \geq 0$
>	$a_k = 3 \cdot 2^k + 2 \cdot 5^k$                      **-(1)**
>	$a_{k+1} = 3 \cdot 2^{k+1} + 2 \cdot 5^{k+1}$           **-(2)**
>Now consider $n=k+2$ 
>	$a_{k+2} = 7a_{k+1} - 10a_{k}$ 
>Then plug in $a_k$ and $a_{k+1}$
>	$a_{k+2} = 7(3 \cdot 2^{k+1} + 2 \cdot 5^{k+1}) - 10(3 \cdot 2^k + 2 \cdot 5^k)$
>	$a_{k+2} = 7(3)(2) \cdot 2^k + (7)(2)(5) \cdot 5^k - (10)(3) \cdot 2^k - (10)(2) \cdot 5^k$
>	$a_{k+2}$ = $(42 \cdot 2^k) + (70 \cdot 5^k) - (30 \cdot 2^k) - (20 \cdot 5^k)$
>	$a_{k+2}$ = $12\cdot2^k +50\cdot5^k$
>	$a_{k+2} = 3(2^2)(2^k) + 2(5^2)(5^k)$
>	$a_{k+2} = 3\cdot2^{k+2} + 2\cdot5^{k+2}$
>	$a_{k+2} = a_n \space \Box$

## Trominoes Proof
**Proposition (Predicate)**
- $2^n \space x\space 2^n$  grid removed one square (in any location) can be covered by L-shaped trominoes
**Proof:** 

## Tower of Hanoi
- Similar in style to the trominoes
- Objective of the game is is to move all disks over to tower 3
	- however, you cannot place a smaller disk a top a larger
	- **Will always take $2^n-1$ moves where n is the number of disks
![[TowerOfHanoi.png]]
Proof:**
	<u>Base Case</u>
	When $n=1$
		$2^1 - 1 = 1$
<u>Induction Hypothesis</u>
	Assume the result $n=k, k \geq 1$
		Then a stack with k disks can be moved to any other tower with $2^k - 1$ moves
<u>Induction</u>  $n=k+1$
	1. Number of moves to move k stack to tower B      = $2^k -1$
	2. Number of moves to move 1 to tower C                = 1
	3. Number of moves to move k stack to tower C     = $2^k-1$
	4. Sum up the number of moves $$(2^k-1)+(1)+(2^k-1) = 2^k+2^k1 = 2(2^k) - 1 = 2^{k+1}-1$$


