
---
aliases: [ "20230907105904",  ]
tags: COMSC, COMSC.335
date_created: 2023-09-07 10:59
---
# Finite Automata and Regular Languages
---
## Overview
- Present the idea of subprograms via finite automata
- Describe the difference between a DFA and a NFA
- Describe why a NFA is not more powerful than an equivalent DFA
- Convert a NFA to a DFA

### Subprograms
- Methods could be used to build larger and more complex programs
	- A method is a subprogram - which can be implemented in a FA, so we should be able to combine Finite automatas
- Before building and reducing machines, we need some concept to ensure we are not changing what each component should be accepting (Equivalence)
	- The labels of the states do not matter
	- The number of states does not matter
	- The presence of  λ does not matter
		- The only thing that matters is that the *languages must be the same*

### NFA vs DFA
- NFA is typically easier to design
	- Only need to account for what you will accept
	- Can let anything you don't want end in a dead state
	- Based on 'striving' for acceptance
- DFA is easier to implement
	- Can account for all inputs
	- Can identify what happens at all time
- But is the NFA more **Powerful**?
	- Can it accept something a DFA cannot

- DFA
	- L(M) = 
![[Screenshot 2023-09-07 at 11.26.49 AM.png]]
- NFA
	- L(M) =
![[Screenshot 2023-09-07 at 11.27.53 AM.png]]
#### Every NFA can be converted to a DFA
- Theorem 2.2
	- Concept is based on replacing transitions and building new states (vertices) which may represent a set of states in the original NFA
	- It works because in an NFA every state transitions to a member of $2^Q$ subsets. That may be a big number, but it is finite!
- **The 'algorithm' to make a NFA = DFA**
	- Algorithm is not the same as program - much more 'squishy'
	- Ensure EVERY state in the converted diagram accounts for EVERY element of the alphabet but be aware of potential trap states
	- Expect to see an increase in the number of states and the number of transitions in a DFA than the NFA (WHY?)

##### Algorithm
1. Create a start state ($q_0$, and all states reach by 'jumping' from $q_0$)
2. From the new start create a single new state composed of EVERY state attained by each element of $\sum$ and subsequent jumps
	- If an element is not represented, develop the trap state
	- If ANY state is a final state, then the new state is a final state
3. For each new state create a single state for each transition of an element from all the incorporated states
	- If an element is not represented, develop the trap state
	- If ANY state is a final state, then the new state is a final state
4. Repeat 3 as required 

>[! bug] Warning
>Pay close attention to bookkeeping. Most errors are due to forgetting to add trap states of forgerring elements of $\sum$

###### Example
- **NFA**
![[Screenshot 2023-09-07 at 11.45.52 AM.png]]
- **List of Transitions**
$\delta(S,a)={p,r,t}$ 
$\delta(S,b)={r,t}$ 
$\delta(prt,a)={t}$ 
$\delta(prt,b)={S,t}$ 
$\delta(rt,a)={t}$ 
$\delta(rt,b)={t}$ 
$\delta(t,a)={\emptyset}$ 
$\delta(t,b)={t}$ 
$\delta(st,a)={prt}$ 
$\delta(st,b)={rt}$ 
$\delta(\emptyset,a)={\emptyset}$ 
$\delta(\emptyset,b)={\emptyset}$

- **Unoptimized DFA**
![[Screenshot 2023-09-07 at 11.55.34 AM.png]]

#### Minimization
- Eliminating redundant states, efficient use of space in subsequent implementation
- Based on the idea of "equivalence"
	- From where we are, there is not apparent difference to where we can go
	- All final states are created equal and all non-final states are equal, the sets are $F$ and $\lnot F$ 
	- If a transition from one state goes someplace different than its set \, it is not equivalent and forms a new set of states
	- Any set with $q_0$ is an initial state, any set with an element of F is a final state
	- Quirky notation --- Rule 3 page 67 "all *a* $\in \sum$" here *a* is any element of $\sum$ 

>[! note] Minimize an NFA
>- Convert the NFA to a DFA
>- Then Minimize the DFA to its most efficient

![[Screenshot 2023-09-07 at 12.09.27 PM.png]]


![[Screenshot 2023-09-07 at 12.16.37 PM.png]]
M(L) = (a+b)a(a+b)*

### Regular Expressions
- W is a regular expression if it can be built from primitives using the above in a finite number of steps
- If $r_1$ and $r_2$ are regular expressions then 
	- $L(r_1 + r_2) = L($