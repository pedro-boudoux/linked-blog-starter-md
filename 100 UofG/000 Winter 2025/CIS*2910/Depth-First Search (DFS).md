**Class:** [[Discrete Structures in Computing II]]
**Date:** 12-04-2025
**Topics:** [[Trees]], [[Algorithms]]

*Depth-First Search* *(DFS)* is a graph traversal algorithm with a goal of systematically exploring all the vertices of a graph. *DFS* goes deep into the graph and produces trees with longer paths from the start vertex.

## Depth-First Search
Below is the *pseudocode* for *DFS*
```python
visit(v)

for every neighbor w of v {

	if w not in T {
		add w to T
		add {v,w} to T
		visit(w)
	}
	
}
```

