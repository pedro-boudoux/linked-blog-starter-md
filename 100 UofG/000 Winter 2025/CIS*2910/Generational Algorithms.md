**Class:** [[CIS*2910]]
**Date:** 01-04-2025
**Topics:** #algorithms , [[Data Structures and Algorithms]]

## Generational Algorithms
A *generational algorithm* is an *algorithm* that exhaustively lists all instances of a specific object with *no repetition*.

### Lexicographical Order
To understand what *lexicographical order* is, just think about alphabetical order . A *string* $a_{1} a_{2}...a_n$ is *lexicographically larger* than another string $b_{1} b_{2} ... b_n$ if either:
1. $length(a) > length(b)$ meaning that string $a$ *is longer* than string $b$ and $a_1a_{2}...a_{m}= b_{1} b_{2} ... b_m$.
2. For some $k$ we have $a_{k}> b_k$ and *for all values of $i$* between $1$ and $k-1$, $a_{i}= b_i$.

### Gray Code Order
*Gray code order* is an algorithm where each successive string *differs by a constant amount.* Below is the *gray code order* for binary strings of length 3.

| Gray Code $(n =3)$ |
| ------------------ |
| $000$              |
| $001$              |
| $011$              |
| $010$              |
| $110$              |
| $100$              |
| $101$              |
| $111$              |

