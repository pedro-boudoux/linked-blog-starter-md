**Class:** [[Discrete Structures in Computing II]]
**Date:** 01-04-2025
**Topics:**

## Sets
A *set* is an unordered collection of objects, a set *contains* elements.

A set $A$ and a $B$ are equal if and only if they *contain* the *same elements*.
$$A=B \leftrightarrow \forall x\in A \cup B ,(x \in A \wedge x \in B)$$
### Subsets
A set $A$ is said to be a *subset* of $B$ if and only if *every element* in $A$ is also in $B$.
$$A \subseteq B \leftrightarrow \forall x \in A , (x \in B)$$
A subset $A$ can also be a *proper subset* of $B$ if *every element* in $A$ is also in $B$, but $A$ and $B$ are not the same.
$$A \subset B \leftrightarrow \forall a \in A, \exists b \in B(a \in B \wedge b \notin A)$$
### Set Builder Notation
Sometimes sets contain too many elements for us to manually list, we can use *set builder notation* in order to represent a set without manually writing every single element.
$$S = \{ x | \text{ criteria } \}$$
Here is an example of set builder notation being used to list a set that only contains even numbers:
$$E = \{ x : 2 \mid x \}$$
### Power Sets
The power set of a set $S$ is the *set of all subsets* of $S$. It can be denoted as:
$$P(S)$$
The *cardinality* of $P(S)$ is:
$$|P(S)| = 2^{|S|}$$
### Cartesian Products
The *Cartesian product* of two sets $A$ and $B$, denoted as $A \times B$, is the set of all possible ordered pairs where the first element comes from $A$ and the second from $B$.
$$A \times B = \{ (a,b) \mid a \in A \text{ and } b \in B\}$$
### Set Operations
There are different operations that can be performed on sets.

#### Union
The *union* of two sets $A$ and $B$, denoted as $A \cup B$, contains all elements in both $A$ and $B$.

#### Difference
The *difference* of two sets $A$ and $B$, denoted as $A-B$, contains all the elements in $A$ but not in $B$.

#### Intersection
The *intersection* of two sets $A$ and $B$, contains all the elements in both $A$ and $B$.

#### Disjoint
Two sets $A$ and $B$ are *disjoint* if and only if $A \cap B = \emptyset$.
