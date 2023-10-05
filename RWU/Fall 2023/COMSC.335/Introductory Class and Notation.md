
---
aliases: [ "20230831110306",  ]
tags: COMSC, COMSC.335
date_created: 2023-08-31 11:03
---
[[COMSC.335 Index]]
# Introductory Class and Notation
---
## Set Notation (Chapter 1.1 in Textbook)
A (Upper Case )$\rightarrow$ Set
a (lower case letter) $\rightarrow$ Member of a set
- **Union** 
	- $\cup$
- **Intersection**
	- $\cap$
- **Difference**
	- $S_1 - S_2$
- **Complement**
	- Everything that is not in the set that we are looking at
- **Cartesian Product**
	- $S x C$
		![[Screenshot 2023-09-05 at 10.14.17 AM.png]]
- **A more explicit notation for sets**
	- $S =${$i : i > 0, i \text{ is even}$}
		- This is read as S is the set of all i, such that i is greater than zero and i is even
- **Empty set (null set)**
	- $\emptyset$
- **Disjoint**
	- If S1 and S2 have no common elements, aka $S_1 \cap S_2 = \emptyset$
- **Finite**
	- A set is to be finite if it contains a finite number of elements, otherwise it is infinite. The size of a finite set is denoted by |S|
- **Powerset**
	- A given set normally has many subsets. The set of all subsets of a set S is called the powerset of S and is denoted by $2^S$
>[! example] Powerset
>If S is the set {a, b, c}, then its powerset is $$2^S = \{\emptyset, \{a\}, \{b\}, \{c\}, \{a, b\}, \{a, c\}, \{b, c\}, \{a, b, c\}, \}$$
>- Here $|S| = 3$ and $|2^S| = 8$. This is a general result; if S is finite, then $$|2^S| = 2^{|S|}$$
- **Partitian**
	- A set can be divided by seperating it into a number of subsets. Suppose that S1, S2, ... Sn are subsets of a given set S and that the following holds:
			  1. The subsets $S_1, S_2,... S_n$ are mutually disjoint
			  2. $S_1 \cup S_2 \cup ... \cup S_n = S$
			  3. None of $S_i$ are empty
	- Then $S_1, S_2,...S_n$ are a partisan of S

- See also functions, equivalence, proof by contradiction and proof by induction

## Three Basic Concepts (1.2)
### Languages
- We need a hard definition of languages
		- So we start with the nonempty set $\sum$ of symbols, called the *alphabet*
		- From the individual symbols, we construct *Strings* which are finite sequences of symbols from the alphabet
			- With a few exceptions, we typically use lowercase letters for elements of $\sum$ and $u , v, w$ for string names
			- The *Concatenation* of two strings $w$ and $v$ is the string obtained by appending the symbols of $v$ to the right end of $w$
			- The *Reverse* of a string is obtained by writing the symbols is reverse order. This is designated by $w^R$ 
			- The *Length* of a string $w$ is denoted by $|w|$ 
				- The *empty string* is a string with no symbols at all. It will be denoted by $\lambda$
					- | $\lambda$ | = 0
			- Any string of consecutive symbols in some w is said to be a *substring* of w
				- $w = vu$
				- then the substrings v and u are said to be a prefix and a suffix of w, respectively
		- $\sum$ * = All possible combinations of the alphabet; all the possible strings, including the empty string
		- $\sum$+ = All the possible strings of the alphabet that have at least one element
	- A language is defined very generally as a subset of $\sum$ *
	- A string in a language L will be called a *sentence* of L
	![[Screenshot 2023-09-05 at 10.39.59 AM.png]]
### Grammars
- To study languages mathematically, we need a mechanism to describe them. Everyday language is imprecise and ambiguous, so informal descriptions in English are often inadequate
- As we proceed we will learn about several language-definition mechanisms that are useful in different circumstances. Here we introduce a common and powerful one, the notion of a *grammar*
	- A grammar for the english ;language tells us whether a particular sentence is well formed or not
	- If we were to give a complete grammar, then in theory, every proper sentence would be explained this way
### Automata

## String Notation
$\sum$ = Alphabet; the set of elements allowed as the input
$\sum$ * = All possible combinations of the alphabet; all the possible strings, including the empty string
$\sum$+ = All the possible strings of the alphabet that have at least one element

*w* = an arbitrary string (italicized)
*v* 

$\lambda$ = empty string NOT a BLANK or SPACE
| $\lambda$ | = 0
$\Delta$
