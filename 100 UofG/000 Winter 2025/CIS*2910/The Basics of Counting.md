**Class:** [[Discrete Structures in Computing II]]
**Date:** 01-04-2025
**Topics:** #combinatronics #enumeration, [[Permutations and Combinations]], [[Binomial Coefficients]]

## The Basics of Counting
*Combinatronics* is the study of the arrangement of objects and *enumeration* is the counting of objects with certain properties. For ways of counting *permutations* and *combinations*, see [[Permutations and Combinations]].

## Counting Rules and Principles
### Product Rule
The number of ways to do a procedure that consists of $n$ tasks is the product of the number of ways you can do each task. 
$$\text{\# ways to do a task} = \prod ^{n}_{i=1} \text{\# of ways to do task }i$$
### Sum Rule
If a task can be done in either $n_1$ or $n_2$ ways (where $n_1$ and $n_2$ are disjoint) then there are $n_{1}+ n_2$ ways to do the task.

### Principle of Inclusion/Exclusion
The *principle of inclusion/exclusion* is a principle used to count numbers in overlapping groups without accidentally double counting.
![[Inclusion Exclusion Example.png]]
#### Principle of Inclusion/Exclusion for 2 Groups
$$\mid A \cup B \mid = |A| + |B| - |A \cap B|$$
#### Principle of Inclusion/Exclusion for 3 Groups
$$\mid A \cup B \cup C \mid = |A| + |B| + |C| - |A \cap B| - |A \cap C| - |B \cap C| + |A \cap B \cap C|$$

### The Pigeon Hole Principle
The *pigeon hole principle* is a principle that states that if $N$ objects (pigeons) are placed into $k$ boxes (pigeon holes), then there is at least one box containing at least $\left \lceil {N / k} \right \rceil$.
