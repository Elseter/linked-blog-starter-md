
---
aliases: [ "20221020154600",  ]
tags: RWU, MATH.221, Math, DiscreteMath
date_created: 2022-10-20 15:46
---
[[MATH.221 INDEX]]
# Computations
---
## Propositional Logic
### Purpose:
	Logical arguments (Atoms)
		- we need to analyze logical arguments and their structure
### Definition: Proposition / Statements
- A proposition / statement is a sentence which is either true or false, but not both

### Definition: Propositional Variables
	Notation: Lower case letters
	- for any proposistional variable there are two possibilities (binary) 
		- True
		- False
In general, we say 'propositions instead of in the position of propositional variables when speaking

### Definition: Propositional Algebra/Calculus
	Compound prepositions
		- Logical 'And' (^)
		- Logical 'Or'  (∨)
		- Negation      (~)
Logical Equivalences
- Two compound propositions are said to be equivalent if they share the same truth values/truth value columns
#### Examples of Basic Truth Tables
'And' Truth Table
|  p  |  q  | p ^ q |
|:---:|:---:|:-----:|
|  T  |  T  |   T   |
|  T  |  F  |   F   |
|  F  |  T  |   F   |
|  F  |  F  |   F   |

'or' Truth Table
|  p  |  q  | p ∨ q |
|:---:|:---:|:-----:|
|  T  |  T  |   T   |
|  T  |  F  |   T   |
|  F  |  T  |   T   |
|  F  |  F  |   F   |

Negation
|  P  | ~P  |
|:---:|:---:|
|  T  |  F  |
|  F  |  T  |



### More Propositional Rules
**Tautologies**
- A propositional statement that has a truth table with only truths. <u>Always True</u>
	- Represented often with the variable: t
**Contradictions**
- A propositional statement that has a truth table with only false. <u>Always False</u>
	- Represented often with the variable: c

**Logical Implications**
|  p  |  q  | p → q |
|:---:|:---:|:-----:|
|  T  |  T  |   T   |
|  T  |  F  |   F   |
|  F  |  T  |   T   |
|  F  |  F  |   T   |

### Conditional Statements
**Implication**
Ex.) 
> If I study hard, I will pass the exam
	- if p then q
	   p → q
- This is written as <u>p implies q</u>
$$ p \to q \equiv \lnot p \lor q $$
Truth Table 
|  p  |  q  | p → q |
|:---:|:---:|:-----:|
|  T  |  T  |   T   |
|  T  |  F  |   F   |
|  F  |  T  |   T   |
|  F  |  F  |   T   |
- The last two lines are true ' by default' aka "Vacuously true"
