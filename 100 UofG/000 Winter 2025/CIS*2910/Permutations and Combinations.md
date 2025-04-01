**Class:** [[CIS*2910]]
**Date:** 01-04-2025
**Topics:** #counting #permutations

## Permutations
A *permutation* is a way to arrange distinct objects from a *set of objects*. An *r-permutation* is an ordered arrangement of $r$ elements from a set containing $n$ items. ($n$-set).
The *number of ways* to *arrange* $r$ objects from $n$ total objects is denoted:
$$P(n,r) = \frac{n!}{(n-r)!}$$
### Permutations with Repetitions
The *number of different permutations* when there's *repetition of elements* can be counted with the following formula:
$$\text{\# of Permutations} = \frac{n!}{n_{1}! \times n_{2!}\times ... \times n_{k}!} $$
where $n$ is the *total number of letters/symbols*.
$n_{1}, n_{2}, ..., n_k$ is the *total number of occurrences* of each distinct symbol.
$k$ is the *number of total distinct symbols*.

## Combinations
A *combination* is an *unordered* selection of distinct elements from a set. An *r-combination* is an unordered selection of $r$ elements from a set containing $n$ items. An *r-combination* is a *subset* of size $r$ from a set of size $n$. The *number of combinations* of size $r$ from a set of size $n$ can be calculated with:
$$C(n,r) = {n\choose r} = \frac{n!}{r!(n-r)!}$$
### Formulae for Different Complex Combination and Permutation Problems

|                         | No Restrictions<br>(only positive $m$ and $n$) | At most one per bin <br>($m$ bust be at least $n$) | Same number of balls in each bin<br>($m\mid n$) |
| ----------------------- | ---------------------------------------------- | -------------------------------------------------- | ----------------------------------------------- |
| Indistinguishable Balls | $$n+m-1 \choose m-1$$                          | $$m \choose n$$                                    | $$1$$                                           |
| Distinguishable Balls   | $$m^2$$                                        | $$P(m,n)$$                                         | $$\frac{n!}{((\frac{n}{m})!)^m}$$               |

