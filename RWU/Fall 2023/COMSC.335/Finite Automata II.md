
---
aliases: [ "20230905105642",  ]
tags: COMSC, COMSC.335
date_created: 2023-09-05 10:56
---
# Finite Automata II
---
[[COMSC.335 Index]]
## Finite Automata II - Nondeterministic Finite Automata
- **Goals** 
	- Define a Nondeterministic Finite Automata
	- Develop a NFA diagram
	- Homework 1 is out there (soon)
		- Sometime later today (09- 05- 23)

### Finite State Automata (FSA or FA)
- Finite because everything is known
	- Q -- All the states
	- $\sum$ -- All the input (alphabet)
	- $\delta$ -- How to go from one state to another ($Qx\sum \rightarrow Q$) 
	- $q_0$ -- Where to start ($q_0 \in Q$)
	- F -- Where to end for acceptance ($F \subseteq Q$)
- M = ($Q, \sum, \delta, q_0, F$) is the definition of a FSA

	- Create a 7 character code with at least one of each
		- S = set of special characters 
		- L = set of Letters
		- D = set of Digits (0 - 9)
			- Not the same as a number
			- number is a composite of digits

#### Deterministic Finite Automata (DFA)
- Can only go to once state on any given input
- Transition is only one state at a time
- Every state must account for every input
- NO MEMORY
- Configuration is based on where it has left to go

- L(M) = {$w \in \sum * : \delta * (q_0, w) \in F$}

#### Nondeterministic Finite Automata (NFA)
- Finite because everything is known
	- Q -- All the states
	- $\sum$ -- All the input (alphabet)
	- $\delta$ -- How to go from one state to another ($Qx(\sum \cup \lambda) \rightarrow 2^Q$) 
	- $q_0$ -- Where to start ($q_0 \in Q$)
	- F -- Where to end for acceptance ($F \subseteq Q$)

- $2^Q$ is the power set of Q, or the set of all subsets of Q including Q and the empty set
- M = ($Q, \sum, \delta, q_0, F$) is the definition of a NFA
##### New and Old 
- Can to to multiple states on the same input -  (new)
- Can "jump" to other states on an empty string $\lambda$ -  (new)
- Transition is not necessarily one state at a time - (new)
- There may be a 'dead state' assumption - (new)
- NO MEMORY - (same)
- Configuration is based on where it has left to go - (same)

- The opportunity to go to multiple places on the same input
- The choice is non-predictable, nor is it repeatable
- NFA 'strives' for acceptance (AKA "guesses")
- Acceptance is attained for a string if ANY sequence results in a favorable state

- Acceptance is attained for a string if ANY sequence results in ending in a favorable state

L(M) = {$w \in \sum * : \delta * (q_0, w) \cap F \neq \emptyset$}
- Language of all strings in the alphabet whose transitions result in a favorable state
- IF ANY TRANSITIONS BRING YOU TO A FAVORABLE STATE, you are accepted
	- You might need to go through every possible sequence to find that acceptable path
	- Goal is to find the first transition that is successful

##### The $\lambda$ - transition
- Consider this as an empty string, or commonly called a "jump"
- A path is the way you travel from one point to another
- A walk is how long it takes for you to get there
	- In a DFA, the length of a walk is |w|
		- The size of your string, as you can only go one place at a time
	- In a NFA, the length of a walk $\leq$ $\Delta$ + (1 + $\Delta$)|w|
		- $\Delta$ = # $\lambda$ in graph
			- number of $\lambda$ in graph

##### Why use a NFA
>[! bug] Note
>- ALWAYS NAME YOUR STATES
>- a start mark (>)
>- Show where you finish (end state)

- NFA allows for multiple success conditions
	- Example in class shows a diagram that has success conditions for strings containing the substring aa or bb 
	- Allows for OR results

#### NFA vs DFA
- NFA is typically easier to design
- Typically only need to diagram the 'successful' machine
	- Missing transitions imply they would be 'trap'
	- Path length typically implies shortest length
	- ANY TRANSITION YOU LEAVE OUT IS ENTERPRITED AS DEAD SPACE
- DFA is easier to implement

>[!Bug] What irks the professor
> Properly erase extra drawn lines in a diagram
> - avoid crossing lines at all costs
> - Don't squiggle out lines
> - If you must cross a line, make an arc 
##### Examples
- Complement of the language shown in fig 2.8
	- fig 2.8 accepts 3 consecutive a's and even number of a's greater than 0
- 

