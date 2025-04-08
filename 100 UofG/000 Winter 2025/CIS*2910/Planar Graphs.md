**Class:** [[CIS*2910]]
**Date:** 01-04-2025
**Topics:** #graphs #conectivity

## Planar [[Graphs]]
A graph representation of a graph, $G = (V,E)$ is *planar* if it has no edges crossing each other.
A *planar graph* has *regions* which are areas of the graph separated from other areas by *edges*. 

### Conditions for a graph to be Planar
If a graph is *planar* then it must satisfy the following 2 conditions:
1. Have a vertex of degree less than 6.
2. $m \leq 3n-6$ 
NOTE: helps to know the *Handshaking Theorem* (see in [[Graphs]]).

### Theorems of Planar Graphs

#### Euler's Formula
If $G$ is a *connected simple planar graph* with $n$ vertices and $m$ edges, then the number of regions in a planar representation, $r$, is:
$$r = m - n + 2$$

#### Kuratowski's Theorem
The *subdivision* of an edge $(u,v)$ replaces the edge $(u,v)$ with two new edges $(u,w)$ and $(w,v)$, *adding a new vertex* $w$.

Two graphs $G$ and $H$ are said to be *homeomorphic* if they can be obtained from the same graph by a sequence of *subvisions*.

A graph is said to be *non-planar* if and only if it contains a subgraph *homeomorphic* to $K_{3,3}$ or $K_5$.


