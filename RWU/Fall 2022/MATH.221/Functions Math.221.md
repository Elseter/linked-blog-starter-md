
---
aliases: [ "20221114093122",  ]
tags: RWU, MATH.221, Math, DiscreteMath
date_created: 2022-11-14 09:31
---
[[MATH.221 INDEX]]
# Functions
---
## Structure
### CONTEXT of Functions

| Domain | Co-Domain |
|:------:|:---------:|
|   1    |     a     |
|   2    |     b     |
|   3    |     c     |
- Every item in the Domain should have a corresponding component in the Co-domain

A function $\mathscr{f} \text{ : } A \rightarrow B$
- A is the Domain
- B is the Co-domain
- From A to B
		-  Is a *Relation* that maps every element in A to a **unique** element in B

| Domain | Co-Domain |
|:------:|:---------:|
|   1    |     a     |
|   2    |     a     |
|   3    |     b     |
- **This is a function**, multiple elements in the domain may have the same co-domain

| Domain | Co-Domain |
|:------:|:---------:|
|   1    |     a     |
|   1    |     b     |
|   2    |     c     |
|   3    |     c     |
- **This is NOT a function**, 1 does not have a unique element in the co-domain

| Domain | Co-Domain |
|:------:|:---------:|
|   1    |     a     |
|   2    |     b     |
|   3    |           |
- **This is NOT a function**, 3 does not have a unique element in the co-domain

### One-to-One Functions
- A function that passes both the horizontal and vertical line tests
	- Where each line will only intercept the graph at a unique point

>[!definition] Definition
>A function $\mathscr{f}$ : $A \rightarrow B$ is defined to be one-to-one, if 
>$$\forall x_1,x_2 \in A, x_1 \neq x_2 \Rightarrow \mathscr{f}(x_1) \neq \mathscr{f}(x_2)$$
>OR $$\forall x_1,x_2 \in A, \mathscr{f}(x_1) = \mathscr{f}(x_2) \Rightarrow x_1 = x_2 $$

### Example Problems 
##### 1.) Not (1-1)
Let $\mathscr{f}$ : $\mathbb{R} \rightarrow \mathbb{R}$, given by $\mathscr{f}(x) = x^2$
	$\mathscr{f}(-1) = \mathscr{f}(1)$ , and hence f is not one to one

##### 3.)
Let $\mathscr{f}$ : $\mathbb{R} \rightarrow \mathbb{R}$, given by $\mathscr{f}(x) = \frac{2x-1}{3}$
Show that $\mathscr{f}$ is 1-1
>[!example] Proof
>Let $x_1, x_2 \in \mathbb{R}$
>Suppose $\mathscr{f}(x_1) = \mathscr{f}(x_2)$
>This gives $$\frac{2x_1 -1}{3} = \frac{2x_2 - 1}{3}$$
> $2x_1 - 1 = 2x_2 -1$
> $2x_1 = 2x_2$
> $x_1 = x_2$

##### 5.)
Let g : $\mathbb{R} \backslash$ {-1} $\rightarrow \mathbb{R}$, be $g(x) = \frac{2x}{x+1}$
<u>Show that g is 1-1</u>
>[! example] Proof
>Let $x_1, x_2 \in \mathbb{R} \backslash${-1}
>Assume, $g(x_1) = g(x_2)$
>This gives, $$\frac{2x_1}{x_1 + 1} = \frac{2x_2}{x_2 + 1}$$
>$2x_1(x_2 +1) = 2x_2(x_1 +1)$
>$x_1(x_2 +1) = x_2(x_1 +1)$
>$x_1 x_2 + x_1 = x_2 x_1 + x_2$
>$x_1 = x_2$

##### 7.)
Let $\phi$ : $(-1, 1) \rightarrow \mathbb{R}$ , be given by $\phi(x) = \frac{x}{x^2 + 1}$ 
Then $\phi$ is (-1, 1)
>[! example] Proof
>Let $x_1,x_2 \in (-1, 1)$
>Suppose, $\phi(x_1) = \phi(x_2)$
>This gives, $$\frac{x_1}{x_1^2 + 1} = \frac{x_2}{x_2^2 + 1}$$
>$x_1 x_2^2 + x_1 = x_2 x_1^2 + x_2$
>$x_1 x_2^2 - x_2 x_1^2 + x_1 - x_2 = 0$
>$x_1 x_2(x_2 - x_1) - (x_2 - x_1) = 0$
>$(x_2 - x_1)(x_1 x_2 - 1) = 0$
>SEE MID-STEP
>$\therefore x_2 -x_1 = 0$
>$\therefore x_2 = x_1$

>[! note] Mid-Step
>WHY
>$x_1 x_2 -1 \neq 0$
>If $x_1 x_2 -1 = 0$
>Then $x_1 x_2 = 1$
>$$x_1 = \frac{1}{x_2}$$
>But $x_1 \in (-1, 1)$, also $x_2 \in (-1, 1)$
>This can also be written as $|x_1| < 1$ and $|x_2| < 1$
>Now $$\frac{1}{|x_2|} > 1$$
>But this is a contradiction

