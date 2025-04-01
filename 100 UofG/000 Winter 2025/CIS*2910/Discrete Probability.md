**Class:** [[CIS*2910]]
**Date:** 01-04-2025
**Topics:** [[Sets]], [[The Basics of Counting]], [[Permutations and Combinations]]

## Discrete Probability
An *experiment* is a procedure that yields one of a given set of possible outcomes. 
The *set of possible outcomes* in an experiment is called the *sample space*. 
An *event* is a subset of the *sample space*. 

The *probability* of an event $E$, which is the subset of a *finite sample space* $S$ where *each outcome is equally likely* is given by:
$$p(E) = \frac{\mid E \mid}{\mid S \mid}$$

### Probability of Complement Events
Let $E$ be an event from a sample space $S$. The probability of event $\overline{E}$, the complement of $E$, which essentially means "anything but $E$", is given by:
$$p(\overline{E}) = 1 - p(E)$$

### Probability Theory
#### Properties of Probabilities
If $S$ is a finite *sample space* with $n$ possible outcomes: $x_1,x_2,x_3,...,x_n$. To assign probabilities to each event the following two conditions have to be satisfied:
1. $0 \leq p(x_{i)}\leq 1$, the probability of an event $x_n$ has to be a value between $0$ and $1$.
2. $\sum\limits^{n}_{i=1}p(x_{n})= 1$ , the sum of all probabilities is equal to $1$.

#### Uniform Distribution
A sample space $S$, with $n$ elements is said to have *uniform distribution* if the probabilities of all outcomes in $S$ are equal to $1 / n$.

#### Probability of an Event
The *probability of an event* $E$ happening is the sum of all probabilities of the outcomes within $E$.
$$p(E) = \sum\limits_{s\in E} p(s)$$
#### Conditional Probability
The *conditional probability* given two events $E$ and $F$, is the probability of $E$ happening given that $F$ already happened is denoted:
$$p(E\mid F) = \frac{p(E \cap F)}{p(F)}$$
### Independence
Two events $E$ and $F$ are independent if the probability of either happening is not affected by the other having already happened. 
$$E \text{ and } F \text{ are independent} \leftrightarrow p(E \cap F) = p(E) \times p(F)$$
### Bernoulli Trials
A *Bernoulli Trial* is a performance of an experiment that only has two possible outcomes, called a *success* and a *failure*. Where $p$ denotes the *probability* of a *success* and $q$ denotes the *probability* of a *failure*. $p+q=1$ meaning that $p = \overline{q}$ (and vice versa). The *probability* of exactly $k$ successes in $n$ independent *Bernoulli Trials* is:
$$p(X=k)={n \choose k}p^{k} q^{n-k}$$
