
---
aliases: [ "20221109093105",  ]
tags: RWU, MATH.221, Math, DiscreteMath
date_created: 2022-11-09 09:31
---
[[MATH.221 INDEX]]
# Set Algebraic Properties
---
## Algebraic Properties
[[MATH.221 Set Algebraic Properties.pdf]]
[[Set Theory]]
- Geometric meaning of some relations

### Compliment Laws
$A \cup A^c = \mathbb{U}$  and  $A \cap A^c = \varnothing$
	- Where U designates the universal set

### Distribution
	$A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$ 
>[!example] Proof
>Suppose 
>	$x \in A \cap (B \cup C)$
>Then, 
>	$x \in A \text { and } x \in B \cup C$
>This means, 
>	$x \in A \text{ and } x \in B \text{ OR } x \in C$
>This yields
>	$(x \in A \text{ and } x \in B) \text{ or } (x \in A \text{ and } x \in C)$
>Which Implies,
>	$x \in A \cap B \text{ or } x \in A \cap C$
>	$\therefore x \in (A \cap B) \cup (A \cup C)$

### De Morgan's Laws
	$(A \cap B)^C = A^C \cup B^C$
>[!example] Proof
>Let,
>$x \in (A \cap B)^C$
>$x \in \mathbb{U}$ (Universal set)
>$\text{not } x \in (A \cap B)$
>$\text{not } x  \in a \text{ OR } \text{not } x \in B$
>$x \in A^C \text{ or } x \in B^C$
>$x \in A^C \cup B^C$
