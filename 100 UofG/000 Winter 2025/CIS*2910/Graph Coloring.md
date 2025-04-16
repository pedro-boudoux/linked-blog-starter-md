**Class:** [[Discrete Structures in Computing II]]
**Date:** 01-04-2025
**Topics:** #graphs 

## Coloring of Graphs
*Coloring* [[Graphs]] involves the assignment of colours to vertices such that no two adjacent vertices are the same colour.

The *chromatic number* of a graph $G$, is the *least number* of colours necessary to colour it.

### The Four Colour THeorem
The *chromatic number* of a planar graph is always less than or equal to 4.
$$\text{Chromatic Number} \leq 4$$

### The Greedy Coloring Algorithm
- Number the set of possible colors. Assume that there is a very large supply of different colors, even though they might not all be used.
- Order the vertices in any arbitrary order.
- Consider each vertex
in order:  

- Assign a color that is different from the color of 's neighbors that have already been assigned a color. When selecting a color for , use the lowest numbered color possible.