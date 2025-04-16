**Class:** [[Discrete Structures in Computing II]]
**Date:** 01-04-2025
**Topics:** #graphs 

## Methods of Representing Graphs
There are many ways of *representing [[Graphs]]* other than just by *graphing them*. For the explanations here, we will be using the following graph:
![[Graph Example 1.png]]
### Adjacency List
An *adjacency list* is a list of the *vertices* in a graph and the *vertices* that they are *adjacent* to. For the graph above, this is the *adjacency list*:

| Vertex | Adjacent Vertices |
| ------ | ----------------- |
| 1      | 2,3,4             |
| 2      | 1,4               |
| 3      | 1                 |
| 4      | 1,2               |
For *adjacency lists*:
- When checking to see whether or not two vertices are *adjacent*, you may have to scan the entire list: $O(n)$.
- When checking to see what are *all the vertices adjacent* to a vertex, you scan the list: $O(n)$.
### Adjacency Matrix
An *adjacency matrix* is a matrix where each row and column represents a vertex and a spot in the matrix is valued $1$ if the vertices represented by the column and the row that the spot is in are adjacent. For the graph above, this is the *adjacency matrix*:
$$\begin{bmatrix}
0 & 1 & 1 & 1 \\
1 & 0 & 0 & 1 \\
1 & 0 & 0 & 0 \\
1 & 1 & 0 & 0
\end{bmatrix}$$

For *adjacency matrices*:
- When checking to see whether or not two vertices are *adjacent*, we can check this with *a single look up*: $O(1)$.
- When checking to see what are *all the vertices adjacent*, you must scan the entire row: $\Theta (n)$.

