---
aliases: 
tags:
  - COMSC
  - COMSC335
date_created: 2023-09-21 11:10
Index: "[[COMSC.335 Index]]"
---


aliases: [ "20230921111019",  ]

# L07 - Context Free Grammar II
---
## Grammars as Generators
- A series of derivations resulting in a string in the lanuage
- A grammar cannot generate a string that is NOT in the language
Grammars as Parsers
- IS there a set of derivations such that $S \Rightarrow *w$
- The exhaustive membership Algorithm
	- Brute Force method
	- Test all possible

#### Example 
- Example: $S \rightarrow SS | aSb | bSa | \lambda$
	- is w = aabb in the language
#### Problems with brute force
- Issues
	- Extremely tedious and inefficient
	- Can be infinite! (consider w=abb which is not in the language)
	- Example: $S \rightarrow SS | aSb | bSa | \lambda$
- Overcome problems with this approach
	- Suppose we stipulate Grammar cannot have the form 
		- $A \rightarrow \lambda$
		- $A \rightarrow B$
- $S \rightarrow SS | aSb | bSa | \lambda$ becomes $S \rightarrow SS|aSb|bSa|ab|ba$
#### With the replacement approach
- Each production now ensures the string increases in size with each production
	- Once parse string > |w| we can say w is not in L
	- Hence need only 2|w| rounds
	- However still unbelievably inefficient
	- Some efficient parsers work on O(w^3) - more to follow in COMSC440 (compilers)
### Simple Grammar (s-grammar)
$A \rightarrow aX$
$A \in V$
$a \in T$
$X \in V*$
- ($aX_1$) pairings only occur once

$S \rightarrow aS|bSS|c$ s-grammar
$S \rightarrow aS|bSS|aSS|c$
- Not a simple grammar, aS and aSS  repeat the ($aX_1$) pairing

### Ambiguity: two ways to same string
- If you can parse a string 2 of more ways for any w, then that w is ambiguous
- Computers don't like ambiguity

- If L is a Context Free Language for which there is ONE unambiguous grammar then L is unambiguous
- If EVERY grammar that generates L is ambiguous then L is an inherently ambiguous language
	- These are very hard to find
	- Need to know every grammar that generates a language