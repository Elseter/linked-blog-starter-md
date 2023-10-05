
---
aliases: [ "20221202093904",  ]
tags: RWU, Math, MATH.221, DiscreteMath
date_created: 2022-12-02 09:39
---
[[MATH.221 INDEX]]
# Equivalence Relations and Classes
---
## ER and EC Sheet
[[MATH.221 Equivalence Relations and Classes_page_1.pdf]]

## Equivalence Classes
>[!definition] Notation
>$[x] :=$ equivalence class of x
>f
>For Example:
>$[0]$ = {$x \in \mathbb{Z} \space|\space xS0$}
>      = {$x \in \mathbb{Z} \space|\space x - 0 = 7k \text{ for some } k \in \mathbb{Z}$}

## Equivalence Relations
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

### Examples
#### ER&EC.2
>[! info] Provided Information
>The relation $R$ on $\mathbb{Z}$ by $$\forall a,b \in \mathbb{Z} \space, aRb \Leftrightarrow 7|(a-b)$$
>$$\Leftrightarrow a \equiv b \text{ mod 7}$$

##### D.)
If x is an integers that is not related to the integers $0, 1, -5, -3, -8, -16$
Write down the equivalence class of x explicitly 
>[! done] Answer
>$[0]$ = {$..., -14, -7, 0, 7, 14, ...$}  = $[0]$
>$[1]$ = {$..., -13, -6, 1, 8, 15, ...$} = $[1]$
  $[2]$ = {$..., -12, -5, 2, 9, 16, ...$} = $[-5]$
>$[3]$ = {$..., -11, -4, 3, 10, 17, ...$}
>$[4]$ = {$..., -10, -3, 4, 11, 18, ...$} = $[-3]$
>$[5]$ = {$..., -9, -2, 5, 12, 19, ...$} = $[-16]$
>$[6]$ = {$..., -8, -1, 6, 13, 20, ...$} = $[-8]$

#### ER&EC.7
>[! info] Provided Information
>Let $n  \in \mathbb{N}$ and let the relation R on $\mathbb{Z}$ given $a, b \in \mathbb{Z}$ by, $$mRn \Leftrightarrow a \equiv b(mod \space n)$$
>$$\Leftrightarrow n|(a-b)$$
>$$\Leftrightarrow a-b = n\cdot k \text{ for some } k \in \mathbb{Z}$$

##### A.) Write down all equivalence classes of R
>[! done] Reflexive Property ($\forall x \in \mathbb{Z}, xRx$)
>Let $x \in \mathbb{Z}$
>Then, $x-x = 0 = n \cdot 0$
>$\therefore xRx$

>[! done] Symmetric Property ($\forall x, y \in \mathbb{Z}, xRy \Rightarrow yRx$)
>Let $x, y \in \mathbb{Z}$
>Suppose $xRy$
>Now, $x-y = n \cdot k \text{ for some } k \in \mathbb{Z}$ 
>$y-x = n(-k)$
>$\therefore yRx$

>[! done] Transitive Property ($\forall x, y, z \in \mathbb{Z}, xRy \text{ and } yRz \Rightarrow xRz$)
>Let $x, y, z \in \mathbb{Z}$
>Suppose $xRy \text{ and } yRz$
>Then, $$ x-y = n \cdot k \text{ for some } k \in \mathbb{Z}$$
>$$ y - z = n \cdot l \text{ for some } l \in \mathbb{Z}$$
>Substitute, $$ x-z = n(k+l)$$
>$$\therefore xRz$$

>[! done] Equivalence classes
>$\mathbb{Z}_n =$ {$[0], [1], [2], [3], ... [n-1]$}

#### ER&EC.8
>[! Info] Provided Information
> Rational Numbers are actually equivalence classes
> To understand this, consider the relation defined on $A = \mathbb{Z} \space \cdot$ {$\mathbb{Z} -${$0$}} by, $$(a,b)R(c,d) \Leftrightarrow ad =  bc, \space \forall (a,b),(c,d) \in A$$

##### A.) Prove that R is an Equivalence Relation
>[! done ] Reflexive Property ($\forall x \in \mathbb{Z}, xRx$)
>Let $a \in A$
>Then, $a = (x,y) \text{ for some } x \in \mathbb{Z} \text{ and } y \in \mathbb{Z} -${$0$}
>Then,   $xy = xy$
