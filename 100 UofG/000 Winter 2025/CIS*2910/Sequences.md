**Class:** [[CIS*2910]]
**Date:** 01-04-2025
**Topics:** #sequences

## Sequences
A *sequence* $\{a_n\}$ is an *ordered list of elements*. All sequences start with $a_1$ unless stated otherwise. Sequences can be infinite or finite, finite sequences can be called *strings*.

### Subsequences
A *subsequence* of a sequence $s_n$ *contains elements* of $s_n$ in the *same order* as $s_n$.
For example, consider the following sequence $s_n$:
$$s_{n}= 1,2,2,2,3,4,5,6$$
a possible *subsequence* of $s_n$ is $1,3,6$.

### Properties of Sequences
#### Increasing
Every element is greater than the previous element.
$$\forall i \geq 1, (a_{1}< a_{i+1})$$
#### Non-Decreasing
Every element is at least the same value as the one before.
$$\forall i \geq 1, (a_{i}\leq a_{i+1})$$
#### Decreasing
Every element is less than the previous one.
$$\forall i \geq 1, (a_{i}> a_{i+1})$$
#### Non-Increasing
Every element is less than or the same as the one before.
$$\forall i \geq 1, (a_{i}\geq a_{i+1})$$

### Types of Sequences

#### Arithmetic Progression
An *arithmetic progression* is a sequence of the form: 
$$a, a+d, a+2d, a+3d, ...$$
Where $a \in \mathbb{R}$ is the *first term* of the sequence, and $d \in \mathbb{R}$ is the *common difference*.

#### Geometric Progression
A *geometric progression* is a sequence of the form:
$$a , ar, ar^2,ar^3,...$$
Where $a \in \mathbb{R}$ is the *first term* of the sequence, and $r \in \mathbb{R}$ is the *common ratio*.

#### Recurrence Relation
A *recurrence relation* is a sequence $\{ a_n\}$ that expresses $a_n$ in terms of one or more of the previous terms. For example:
$$a_{n}= a_{1} + 2n$$
A *recurrence relation* could be an example of [[Recursion]].

##### Methods for Finding Closed Form Expressions for Recurrence Relations
###### 1. Guess and Check
Look at examples, find pattern, guess it. This approach needs to be verified (by [[Induction]]).

###### 2. Repeated Substitution
Start at the $n^{th}$ term and go backwards to determine the value of the recurrence after $i$ substitutions. Difficult part is *finding the pattern*. Guess must be verified.
