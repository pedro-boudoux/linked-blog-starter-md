**Class:** [[Discrete Structures in Computing II]]
**Date:** 12-04-2025
**Topics:** [[Trees]], [[Algorithms]]

*Breadth-First Search* *(BFS)* is a graph traversal algorithm with a goal of systematically exploring all the vertices of a graph. *BFS* explores the graph by distance from the initial vertex, starting with its neighbors and expanding the tree to neighbors of neighbors, etc.

A *BFS* search tree is likely the preferred spanning tree for broadcasting in a network because it produces the shortest paths from the initial (source) vertex.

## Breadth-First Search
Below is the *pseudocode* for *BFS*
$\text{Input: An undirected, connected graph } G \text{. A start vertex } v_1$
$\text{Output: }T, \text{ a breadth-first search tree.}$

```python
add v1 to T
add v1 to the back of the list

while the list is not empty
	remove vertex v from the front of the list
	for each neighbor w of v that is not already in T:
		add w and {w,v} to T
		insert w at the back of the list
```

