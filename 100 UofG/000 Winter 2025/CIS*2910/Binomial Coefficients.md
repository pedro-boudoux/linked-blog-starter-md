**Class:** [[CIS*2910]]
**Date:** 01-04-2025
**Topics:** 

A *binomial expression* is the sum of *two terms* $x+y$, a *binomial coefficients* are the values that occur as the coefficients in the expansion of $(x+y)^n$, we can consider $n \choose r$ to also be a *binomial coefficient* because its values can occur as the coefficients in $(x+y)^n$ .

## Binomial Theorem
The *binomial theorem* is a theorem used for expanding the power of any *binomial expression* to the power of $n$.
$$(x+y)^{n}= \sum\limits^{n}_{j=0} {n \choose j} \cdot x^{n-j} \cdot y^j$$
### Binomial Identities and Corollaries
#### Corollary 1
$$\sum\limits ^{n} _{j=0} {n \choose j} = 2^n$$
#### Corollary 2
$$\sum\limits^{n}_{j=0} (-1)^{j} \cdot {n \choose k} = 0$$
#### Corollary 3
$$\sum\limits^{n}_{j=0} 2^{j} \cdot {n\choose j} = 3^n$$
#### Pascal's Identity
$${n+1 \choose k} = {n \choose k-1} + {n \choose k}$$
#### "Another One"
$${n + 1 \choose r+1} = \sum\limits^{n}_{j=r} {j \choose r}$$
#### Vandermonde's Identity
$$\text{ if } 0 \leq r < m,n \text{ } \implies \text{ } \sum\limits^{r}_{k=0} {m \choose r-k} {n \choose k}$$
