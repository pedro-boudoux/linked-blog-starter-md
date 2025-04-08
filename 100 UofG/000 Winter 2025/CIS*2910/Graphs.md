**Class:** [[CIS*2910]]
**Date:** 01-04-2025
**Topics:** #graphs 

## Introduction to Graphs
A *graph* is a mathematical structure that represents a relation between a set of objects, *vertices* in this case, where *if two vertices are related* then there exists an *edge* between them.

The *order* of a graph is the *number of vertices* it contains, usually denoted $n$ where $\mid V \mid = n$. The *size* of a graph is the *number of edges* it contains, usually $m$ where $\mid E \mid = m$.

### Simple Undirected Graphs
A *graph* $G = (V,E)$ that consists of a non-empty set of *vertices* $V$ and a set of $E$ of unordered pairs of distinct vertices of $V$ called *edges*.
![[Simple Undirected Graph.png]]
The *max number of edges* of a *simple undirected graph* is $n \choose 2$.
### Multigraph
A *multigraph* is a graph that allows for multiple *edges* between pairs of vertices, meaning that two *vertices* can be connected by more than just one edge. 
![[Multigraph.png]]

### Pseudograph
A *pseudograph* is a *multigraph* that allows *loops* and/or *edges* from a vertex back to itself.
![[Pseudograph.png]]

### Directed Graph
A *graph* $G = (V,E)$ is a *directed graph* if $E$ is a set of *ordered pairs* of elements of $V$. The differences between a *directed graph* and a *simple undirected graph* are as follows:
1. The *edges* are *ordered pairs* meaning that $(u,v) \neq (v,u)$.
2. *Vertices* in a pair *don't have to be distinct* meaning that the loop $(u,u)$ is possible.
 ![[Directed Graph.png]]
 The *max number of edges* in a *directed graph* is $n^2$.

## Representation of Graphs
See [[Methods of Representing Graphs]].

## Theorems

### Handshaking Theorem
The sum of degrees of all vertices is equal to twice the number of edges.
$$\sum\limits_{v \in V} deg(v) = 2m$$
