**Class:** [[CIS*2910]]
**Date:** 01-04-2025
**Topics:** #isomorphism #graphs , [[Connectivity]], [[Graphs]]

## Isomorphism
*Isomorphism* practically means that two [[Graphs]] are the same, they just don't look the same. If two graphs are like that, then they are said to be *isomorphic*. A more formal definition of *isomorphism* is that two simple graphs $G_{1}= (V_{1}, E_1)$ and $G_{2}= (V_{2}, E_2)$ are *isomorphic* if there is a *one-to-one* and *onto* function $f$ such that $f : V_{1}\rightarrow V_{2}$ where:
$$(u,v) \in E_{1} \leftrightarrow (f(u), f(v)) \in E_2$$
The function $f$ is called an *isomorphism*.
![[Isomorphic Graphs.png]]
The two graphs *above* are isomorphic because they are the same, just rotated.
### Degree Sequence
The *degree sequence* of a graph is a sequence listing the *number of edges of each vertex* in the graph, in ascending order.
The *degree sequence* of the graph above is: $2,2,2,2$.

#### Degree Sequences and Isomorphism
If two graphs *don't have the same degree sequence* then they are *NOT isomorphic*. However, if two graphs have the *same degree sequence* it *does not mean* that they are *isomorphic*.


