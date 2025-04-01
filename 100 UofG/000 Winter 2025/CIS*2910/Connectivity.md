**Class:** [[CIS*2910]]
**Date:** 01-04-2025
**Topics:** #graphs 

## Connectivity
*Connectivity* pertains to the ways that the *vertices* in [[Graphs]] are connected and how that affects the properties of the graph.

### Walk
A *walk* is a sequence of vertices $v_0,v_1,v_2,...,v_j$ where there is an *edge* between each *consecutive pair* of *vertices*.

The *length of a walk* is the number of edges in a *walk*.

#### Closed Walk
A *walk* is a *closed walk* where the endpoint is the same as the starting point $(v_0=v_j)$. Meaning that it goes in a circle.

#### Open Walk
A *walk* is an *open walk* where the first and last vertices are distinct $(v_0\neq v_j)$. Meaning that it doesn't go in a circle.

#### Trail
A *trail* is a *walk* with *no repeated edges*.

#### Path
A *path* is an *open walk* with *no repeated edges*.

#### Circuit
A *circuit* is a *closed walk* with *no repeated edges*.

#### Cycle
A *cycle* is a *circuit* of $\text{length} \geq 1$ with *no repeated vertices* except for the *first and last*.

### Cuts
*Cuts* are ways of dissecting and splitting graphs from itself, a vertex is said to be a *cut vertex* if removing it makes the graph *disconnected*.

Let $G = (V,E)$ a subset $V' \subseteq V$ is a *vertex cut* or a *separating cut* if removing all the vertices $V'$ from $G$ makes $G$ disconnected.

![[Cut Graph.png]]
In the graph above, the red vertex is a *cut vertex* because removing it causes the graph to be *disconnected*.

## Connectivity in Directed Graphs
*Directed Graphs* have different connectivity properties than *undirected graphs* because of their directive property.

### Weakly Connected
A *directed graph* is said to be *weakly connected* if the underlying graph (the graph when directions are removed) is *connected*.

### Strongly Connected
A *directed graph* is said to be *strongly connected* if for every pair of vertices $u,v \in V$, there is a path from $u$ to $v$ and from $v$ to $u$. Note that if a graph is *strongly connected*, then it is also *weakly connected*.
