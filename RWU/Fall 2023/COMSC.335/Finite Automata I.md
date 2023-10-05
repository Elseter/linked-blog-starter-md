
---
aliases: [ "20230831111248",  ]
tags: COMSC, COMSC.335
date_created: 2023-08-31 11:12
---
# Finite Automata I
---
[[COMSC.335 Index]]
## What makes an automaton
- limited memory capacity
	- No auxiliary memory
	- reads input from a tape (called words or strings)
	- Changes state with each input
	- At end of input the 'machine' is in a favorable state or an unfavorable state 
	- If the machine ends in a favorable state, then that string is accepted, otherwise it is not
>[! note] Note
>favorable state is used interchangeably with accepting state or final state. Final State Automata are called **Acceptors**

### Finite State Automata (FSA or FA)
- Finite because everything is known 
	- $Q$ : all the states
	- $\sum$ : All the input (alphabet)
	- $\delta$ : How to go from one state to another (function $Q$ x $\sum \rightarrow Q$)
	- $q_0$ : Where to start ($q_0 \in Q$)
	- $F$ : Where to end ($F \subseteq Q$) 

- Deterministic Finite Automata (DFA)
	- Can only go to one state on any given input
	- Transition is only one state at a time
	- **NO MEMORY**
	- Configuration is based on where it has left to go

- $M = (Q, \sigma, \delta, q_0, F$) is the definition of a FSA

#### Examples
##### Soda Machine
- No Change Return
- Coins only, we are not accepting pennies
- Soda Costs 25 cents
- So what do we accept as our input?
	- $\sum$ = {q, d, n}
		- q = quarters
		- d = dimes 
		- n = nickels 
	- Every state must have a transition based on any of the possible inputs

- $Q =$ {$s, 20, 15, 10, 5, f$}
- $\sum$ = {$q, d, n$}
- $q_0$ = $s$
- $F$ = {$f$}
	- It is possible to have more than one final state, so this is a set
- $\delta$ = See Image

ADD IMAGE
##### Two consecutive a's
- What is the input
	- $\sum$ = {$a, b$} *(WLG)*
		- WLG stands for Without Loss of Generality
			- The size of the input set does not change the function of the machine
	- Looking for two consecutive aa's in a string
- Machine will be called $M$
- The language of the machine will be called $L(M)$
	- $L(M) =$ {$w \in \sum ^* : \delta ^* (s, w) \in F$}

- Define the machine
- Q = {$s, a , aa$}
- $q_0$ = s
- F = {$aa$}
- $\delta$ = See Diagram

##### Substring Identifier (001)
- What is the input
	- $\sum$ = {$0,1$}
- We do NOT want the substring of 001

- Define the machine
- Q = {$s, 0, 00, 001$}
- $q_0$ = s
- F = {$s, 0, 00$}
- $\sum$ = {$0, 1$}
- $\delta$ = See Diagram

#### Expand the Idea
- Every finite automata defines the language
- Grouping all the finite automata creates a set of languages called a *family*
- The family of languages accepted by finite automata is called the set of *Regular Languages*
- A language L is regular if and only if there is an acceptor M such that L = L(M)
	- To have a language that is regular, we need a finite automata machine that accepts that languages