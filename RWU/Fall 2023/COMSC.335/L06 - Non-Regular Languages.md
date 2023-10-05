

aliases: [ "20230919110239",  ]
tags: COMSC, COMSC335
date_created: 2023-09-19 11:02

# L06 
---
## COMSC335 Homework and Exams
- A machine has no idea what you "meant"
- A machine has no idea what "it should have done" or what it "should have known"
- A machine only does what you tell it to do

## Non-Regular Languages
### What will we be discussing
- Describe and use the pumping Lemma
- Explain some shortfalls of the pumping lemma
- Define the concept of a context free language
- Develop leftmost and rightmost derivations
- Describe a derivation tree
#### Linear Grammar
- G = (V, T, S, P)
- $A \rightarrow xBy$
- $A \rightarrow z$
- $x, y, z \in T*$ (there may be 0 or any number of terminals)
- Only one variable per production and it may be on the left right or center 
##### Example
- G = ({A, B, S}, {a,b}, S, P)
	- $S \rightarrow A$
	- $A \rightarrow aB$
	- $A \rightarrow \lambda$
	- $B \rightarrow Ab$

- We can NOT make a machine from this grammar
#### Non-Regular Language
- The key is memory needed
- If an automata needs a memory to accept a language it is not a regular language
- The only "memory" an automata can use is the "memory" reflected. by its state
- We use the sense that a regular language must be infinite (others we would know exactly what n is)

- Infinite implies a loop of some nature on a path that leads to a favorable state
- If the expression was Regular, then it also contains a Kleene start (the ability to have the expression concatenated to itself 0 or more times)
- Using the two ideas above, we can generate an infinite number of repetitive substrings
- Or, we should be able to continuously 'pump' a substring of the original string back into the original string

##### the 'pumping lemma' is formed
- Let L be a regular language. There exists an integer m>0 such that any string $w \in L$, with |w| >=m can be represented as the concatenation xyz such that:
	- y is non-empty
	- |xy| ,= m (sometimes this is called the pumping length, p)
	- |y| >= 1
	- $xy^iz \in L$ for i >=0

>[! bug] Proof by Contradiction
>To prove that a language is not regular, we need to prove that the 'pumping lemma' is false for that language
- The pumping lemma can not be used to show that a language is regular

### Finite Automata
	- Used to regonize strings
- A string ending in a favorable states was part of the language
- A string not ending in a favorable states was not part of the language
	- Acceptors
	- Expressions are Descriptors
#### A few more definitions
- The general approach is:
	- If the Left side of a Production is matched in a string, it can be replaced with whatever is on the Right side of the Production
	- The derivation, or replacement using the rule is referenced as $u \Rightarrow v$
	- Any terminal on the Left side is considered the context of the Variable on the left side
	- To be context free, the Left side must be a single variable 

##### Basic Questions
- Are all regular languages context free?
	- Yes
- Are all linear languages context free?
	- Yes
- Are all context free Languages Linear?
	- No
- Are all context free languages regular?
	- No

### Derivation
- Description of the way a string is formed from productions
- Selecting the Leftmost (rightmost) Variable for every derivation is called a leftmost (rightmost) derivation
- Derivation Tree is a graphic depiction of the derivation
	- Leaves are Terminals
	- Inner Nodes are Variables
	- Shows derivation, but no order

- A partial derivation is a sentential form
	- all the leaves of a partial derivation tree
- Ordered Tree
	- Root is S
	- Every leaf is either a terminal or lambda
	- Every interior node is a Variable 
