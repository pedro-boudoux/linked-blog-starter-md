**Class:** [[Discrete Structures in Computing II]]
**Date:** 01-04-2025
**Topics:** [[Graphs]], [[Connectivity]]

## What are Trees?
A *tree* is a connected simple graph that contains *no simple cycle*. 

An undirected graph is a tree if and only if there is a *unique simple path* between any two of its vertices (meaning that there is *exactly one way* of getting from one vertex to another).

### Terminology for Trees
#### Rooted Trees
A *rooted tree* is a tree in which one vertex has been designated as the root and every edge is thought of as being directed away from the root. Below is some terminology for rooted trees:
##### Parent Vertex
The *parent vertex* of a tree is the first vertex encountered after a vertex $v$ along the path from $v$ to the root.
##### Child Vertex
If a vertex $v$ is the *parent* of $u$ then $u$ is the *child* of $v$.
##### Ancestors
The *ancestors* of a vertex $v$ are *all the nodes on a path from the root to* $v$, including the root.
##### Descendants
The *descendants* of a vertex $v$ are all vertices that have $v$ as an ancestor.
##### Leaf
A *leaf* is a vertex in a tree with *no children*.
##### Internal Nodes
An *internal node* is a vertex in a tree with *children*.

#### Ordered Rooted Tree
An *ordered rooted tree* is a *rooted tree* where the children of each internal vertex is ordered.
![[Ordered Rooted Tree.png]]
#### Free Tree
A *free tree* is a tree with no designated root, meaning that it's just a structure of connected nodes without any specific orientation or hierarchy. 
##### How to tell Free Trees apart from Regular Graphs
- If a graph has $n$ nodes and more than $n-1$ edges, then its *NOT a tree*, because it has a cycle.
- If a graph has *fewer than* $n-1$ edges, then its *NOT a tree*, because it is disconnected.
- If a graph has exactly $n-1$ edges, and its connected, *it is a tree*.

#### Subtree
If $v$ is a vertex in a *tree*, then the *subtree* rooted at $v$ is the subgraph containing *all descendants of* $v$.

#### m-ary Tree
A *rooted tree* is an *m-ary* tree if every internal vertex has no more than $m$ children. 
An *m-ary* tree is said to be full if *every internal node* has exactly $m$ children.

#### Forests
A *forest* is a disjoint collection of *one or more* trees. It is an *undirected graph* with no cycles.

## Terms for Trees
The *level* of a tree is the *length of the path* from $v$ to the *root*. The *root* is at *level 0*.

The *height* is the number of levels the tree has in total.

A *rooted* *m-ary* tree is said to be *balanced* if and only if all leaves are at levels $h$ or $h-1$. Below is a picture of a *balanced* *binary tree*.
![[balanced tree.png]]

## Spanning Tree
A *spanning tree* of a connected simple graph $G$ is a subgraph that is a tree containing every vertex of $G$.
![[Spanning tree Example.png]]
### Minimum Spanning Tree (MST)
The *Minimum Spanning Tree (MST)* of $G$ if its *edges are weighted* is a spanning tree whose total weight (sum of weights of its edges) is minimal.

#### Kruskal's Algorithm
*Kruskal's Algorithm* is a greedy algorithm for finding a *minimum spanning tree* in a simple weighted graph $G$. 
Let $w(e)$ denote the weight of edge $e$, below is the *pseudocode* for *Kruskal's Algorithm*:

$\text{Sort edges in increasing order by weight:} w(e_{1})\leq w(e_{2}) \leq ... \leq w(e_m)$ 
$T = \emptyset \text{ (the spanning tree) }$ 
$\text{for } i = 1 \text{ to } m \text{ do }$
	$\text{if } T \cup e_{i} \text{ has no cycle then}$
		$T = T \cup e_i$ 
	
#### Prim's Algorithm
*Prim's Algorithm* is another greedy algorithm for finding the *minimum spanning tree*. It starts with a random *arbitrary* vertex, then adds the smallest edge that connects a new vertex to the growing tree until all vertices are included.