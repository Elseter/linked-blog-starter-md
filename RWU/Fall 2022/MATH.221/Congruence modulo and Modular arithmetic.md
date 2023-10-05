
---
aliases: [ "20221207091042",  ]
tags: RWU, Math, MATH.221, DiscreteMath
date_created: 2022-12-07 09:10
---
[[MATH.221 INDEX]]
# Congruence modulo and Modular arithmetic
---
## Congruence modulo and Modular arithmetic

>[! definition]
>Let $n \in \mathbb{N}$. Let $a, b \in \mathbb{Z}$. Then
>$$ a \equiv b(\text{mod}\space n) \Leftrightarrow n|(a-b)$$
>$$ \Leftrightarrow a = b + n \cdot k \text{ for some } k \in \mathbb{Z}$$
>"a is congruent to b mod n"
>"a and b share the same remainder when divided by n"
>- $a \text{ mod }n = b \text{ mod }n$

>[! note] Secondary Definition 
>$x \text{ mod } n :=$ remainder when x is divided by n

>[! info] Theorem
>Let $n \in \mathbb{N}$
>'Congruence mod n' is an equivalence relation on $\mathbb{Z}$ that generates equivalence classes,
>$$ \mathbb{Z}_n = \{ [0], [1], [2], [3],...,[n-1] \}$$
>This means we have,
>$(I), \space \forall a \in \mathbb{Z}, a \equiv a(\text{ mod } n)$
>$(II), \space \forall a,b \in \mathbb{Z}, a \equiv b(\text{ mod }n) \Rightarrow b \equiv a (\text{ mod }n)$
>$(III), \space \forall a,b,c \in \mathbb{Z}, a \equiv b(\text{ mod }n) \text{ and } b \equiv c (\text{ mod }n) \Rightarrow a \equiv c (\text{ mod }n)$

>[! info] Theorem: Properties of congruence mod n
>Let $n \in \mathbb{N}$, and let $a, b, c, d \in \mathbb{Z}$.
>Suppose $a \equiv c (\text{ mod }n)$ and $b \equiv d (\text{ mod }n)$ then,
>
>$(I) \space \space a+b \equiv c+d (\text{ mod }n)$
>$(II) \space \space a-b \equiv c-d (\text{ mod }n)$
>$(III) \space \space ab \equiv cd (\text{ mod }n)$
>$(IV) \space \space \forall m \in \mathbb{N}, a^m \equiv c^m (\text{ mod }n)$
>
>>[!done] Proof of Property $I$
>>By the assumptions, $a = c + n \cdot k$ and 
>>$b = d + n \cdot l \text{ for some }k,l \in \mathbb{Z}$
>>Then,
>>$$ (a+b) = (c+d) + n(k+l)$$
>>$$\therefore a+b \equiv c+d (\text{ mod }n)$$
>
>>[!done] Proof of Property $IV$
>>Known:
>>$$ a \equiv c (\text{ mod } n) \Rightarrow \forall m \in \mathbb{N}, \space a^m \equiv c^m(\text{ mod } n)$$
>>Proof by induction:
>>
>>**Base case:** 
>>When m=1, the result holds
>>
>>**Induction Hypothesis:**
>>Assume $a^k \equiv c^k(\text{ mod } n) \text{ for all } k \in \mathbb{Z}$
>>
>>**Induction**:
>>>[!info] Side note
>>>When $a \equiv c(\text{ mod } n)$
>>>and $b \equiv d(\text{ mod } n)$
>>>Then $ab \equiv cd(\text{ mod } n)$
>>
>>Then multiplying by $a \equiv c(\text{ mod } n)$:
>>$$ a^{k+1} \equiv c^{k+1}(\text{ mod } n)$$
>>$\therefore$ By mathematical induction the result holds for $\mathbb{N}$

>[! example] Example
>$89 \equiv 1(\text{ mod }4)$ and $31 \equiv 3(\text{ mod }4)$
>When 89 is divided by 4, 1 is the remainder
>Then, 
>1. $89 + 31 \equiv 1+3(\text{ mod }4)$
>$4 \equiv 0(\text{ mod }4)$
>$89-31 \equiv 0(\text{ mod }4)$
>
>2. $89-31 \equiv 1-3(\text{ mod }4)$
>$-2 \equiv 2(\text{ mod }4)$
>$89-31 \equiv 2(\text{ mod }4)$
>
>3. $89 \cdot 31 \equiv 1 \cdot 3(\text{ mod }4)$
>
>4. $89^4 \equiv 1^4 (\text{ mod }4)$
>
>5. $31^4 \equiv 3^4(\text{ mod }4)$
>$3^2 \equiv 1(\text{ mod }4)$
>$(3^2)^2 \equiv 1(\text{ mod }4)$
>$31^4 \equiv 1(\text{ mod }4)$

>[! definition] Unit Digits
>Find the <u>'units digit'</u> of $2^{50}$
>Ans:
>>[! info] Note
>>We're simply doubling both sides then removing the remainder of 10 resulting in only the unit value remaining as the remainder
>>- Then in the final line, I replace 2^5 with its remainder which I know to be 2, then rinse and repeat
>
>$2 \equiv 2(\text{ mod }10)$
>$2^2 \equiv 4(\text{ mod }10)$
>$2^3 \equiv 8(\text{ mod }10)$
>$2^4 \equiv 6(\text{ mod }10)$
>$2^5 \equiv 2(\text{ mod }10)$
>$2^{50} \equiv (2^5)^{10}  \equiv 2^{10} \equiv (2^5)^2 \equiv 2^2 \equiv 4(\text{ mod }10)$

>[! example]
>Problem: What is the remainder when 2^20 is divided by 7?
>Ans:
>$2 \equiv 2(\text{ mod }7)$
>$2^2 \equiv 4(\text{ mod }7)$
>$2^3 \equiv 1(\text{ mod }7)$
>$2^4 \equiv 2(\text{ mod }7)$
>$2^5 \equiv 4(\text{ mod }7)$
>$2^{20} \equiv (2^4)^5 \equiv 2^5 \equiv 4(\text{ mod }7)$

>[! example] Example 2
>Problem: What is the units digit of 3^50?
>Ans:
>$3 \equiv 3(\text{ mod }10)$
>$3^2 \equiv 9(\text{ mod }10)$
>$3^3 \equiv 7(\text{ mod }10)$
>$3^4 \equiv 1(\text{ mod }10)$
>$3^5 \equiv 3(\text{ mod }10)$
>$3^{50} \equiv (3^5)^{10} \equiv 3^{10} \equiv (3^5)^2 \equiv 3^2 \equiv 9(\text{ mod }10)$

>[! example] Example 3
>Solve:
>$\left.\substack{16x+12y=32 \\ 40x-9y=16}\right\} (\mod 3)$
>Ans:
>R

