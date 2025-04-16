**Class:** [[Discrete Structures in Computing II]]
**Date:** 01-04-2025
**Topics:** [[Connectivity]], [[Graphs]], 

## Euler Circuits and Trails

### Euler Trail
An *Euler trail* is an *open trail* that traverses every edge exactly once. If a graph $G$ has an *Euler trail* then it must have *exactly 2 vertices of odd degree*.

An *Euler Trail* begins and ends at an edge with *odd degree*.

### Euler Circuit
An *Euler circuit* is a *circuit* that traverses every edge exactly once. If a graph $G$ has an *Euler circuit* then all of its vertices *must have an even degree*.
If a graph is *connected* and all of its vertices have an *even degree* then it must have an *Euler Circuit*.

## Hamilton Paths and Cycles

### Hamilton Path
A *Hamilton path* is a *path* that visits every vertex exactly once.

### Hamilton Cycle
A *Hamilton cycle* is a path that visits every vertex exactly once (except for the first and last vertex). A graph containing a *Hamilton cycle* is said to be *Hamiltonian*. 

All complete graphs $K_n$ where $n \geq 3$ are considered *Hamiltonian*, and all cycle graphs $C_n$ are also *Hamiltonian*.

#### Sufficient Conditions for Hamilton Cycles
Note that if a graph satisfied all these conditions then it can be said to be *Hamiltonian*, however, a graph does not need to satisfy all these conditions to be *Hamiltonian*. (i.e: $C_5$).
##### Dirac's Theorem
If $G$ is a simple graph with $n \geq 3$ vertices where the degree of every vertex is at least $n/2$, then $G$ is *Hamiltonian*.
##### Ore's Theorem
If $G$ is a simple graph with $n \geq 3$ vertices where every pair of non-adjacent vertices $u$ and $v$ we have $deg(u)+deg(v) \geq n$, then $G$ is *Hamiltonian*.
