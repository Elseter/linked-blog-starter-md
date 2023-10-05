

aliases: [ "20230914110759",  ]
tags: COMSC, COMSC335
date_created: 2023-09-14 11:07

# L05 Finite Automata and Regular Languages
---
## $NFA \leftrightarrow$ Right Linear Grammar
- Machine Definition
	- M = ($Q, \sum, \delta, q_0, F$)
- Grammer
	- G = (V, T, S, P)
	- Q to V
	- $\sum$ to T


### Expresion and Mapping to L
- Automata A which accepts L
- Automata B which accepts M
	- $Q_A \cap Q_B = \emptyset$
		- There are no shared states between the two machines

- We will take the original start states and go back by one state. Creating a new start state. This new start state will traverse to to either of the two start states with a $\lambda$
- This new machine now accepts $L \cup M$ 
	- It is the combination of the two previous machines

>[! bug] SIMPLIFYING
>CAN ONLY SIMPLIFY DFA's 
>- Don't forget to convert

- **Concatenation**
	- Take every favorable state of A and connect using $\lambda$ to start state of B. Order matters
- **Kleene star of A**
	- All states in F use $lambda$ jumps to a new s which is favorable
	- Now accepts L*

#### Expressions and Mapping to L Cont.
- We have original machine A
- We want to create A' which accepts not L
- Complement is more than simply changing the accepting states to non-accepting and changing non-accepting to accepting 
	- THIS REQUIRES A DFA
		- Since dead states are not accounted for in NFA's
		- These dead states also need to be swapped

## Intersections
- Automata A which accepts L
- Automata B which accepts M
	- What does the machine that accepts $L \cap M$ look like?
	- $Q_A \cap Q_B = \emptyset$
		- Make sure states do not have the same name

>[! notes] How to do
>**Step 1.** Create DFA's for both machines
>**Step 2.** Find the cartesian product. Not all of these will be valid. $$ Q = Q_L X Q_M$$
>**Step 3.** Find $q_0$ and F. Combined start state $q_0$ is $q_{M0}q_{L0}$
>**Step 4.** Build $\lambda$. You build a diagram encompassing every transition from every state. If either of the result states are a dead state, then that entire transition goes to a dead state. This will result in 90 transitions leading to a DFA which would need to be minimized
>**HINT**: Only look at the steps that will take you to your favorable states. Start at $q_0$ then build from there. Find only the paths that you are actually going to travel. 
>**Step 5.** Continue this process until there are no unique states on the right side.
>**Step 6.** Draw a horrifying graph


### Properties of Regular Languages
- The previous diagrams show us that Union, Intersection, Concatenation, Complement and * are closed
- Basic Questions
	- Is there a way to prove that a string is a member of L
	- Is there a way to prove a language is Empty, Finite, or Infinite
	- Is there an algorithm to determine if $L_1 = L_2$
		- Means everything in L1 is in L2, everything in L2 is in L1 there is nothin in L1 that is not in L2 and there is nothing in L2 that is not in L1

#### Membership Algorithm
- Run w through M, if it end $\in$ F in L
#### Empty Language
- It doesn't accept any input
- How to tell if it accepts nothing?
- Must have favorable states
- ==No path from $q_0$ to $q_m \in$ F==
#### Finite / Infinite Languages
- An infinite language contains a loop on the favorable path
- Don't count the dead state
	- A finite language is any language that is not infinite

#### Algorithm to determine equality in Languages
- Create a new language called $L_3$
	- $L_3 = (L_1 \cap$ (complement $L_2$) ) $\cup$ (complement $L_1 \cap$ $L_2$ )
		- If $L_3 = \emptyset$ then $L_1 = L_2$
