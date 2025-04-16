**Class:** [[Discrete Structures in Computing II]]
**Date:** 01-04-2025
**Topics:** #functions #domain 

## Functions Review
A *function* is a relation that assigns *exactly one element* of $B$ to each element of $A$. It is written as:
$$f : A \rightarrow B$$
### Domain
The *set* of which $f$ *maps elements from*. The domain of $f$ in the function above is $A$.

#### Domain of Definition
The *domain of definition* of a function $f$, denoted as $D_f$ is the set of all elements in $A$ which have an element of $B$ assigned to them by the function $f$. This basically means that the *domain of definition* is the set of all elements from the original domain that are *used by the function*.
$$D_{f}= \{ x \mid x \in A \wedge \exists f(a) = b\}$$
### Codomain/Target
The *codomain* or the *target* of a function is the set which $f$ maps elements of the domain to. The *codomain/target* of $f$ defined in the example above is $B$.

#### Range
The *range* of a function is the set of elements in the *codomain/target* that are actual outputs of $f$. 
$$R_{f}= \{ b \mid b \in B \wedge \exists f(a) =b\}$$
### Properties of a Function
#### One-to-One/Injective
A function $f$ is *one-to-one/injective* if and only if *two inputs* on $f$ *return the same output*, then the *inputs have to be the same*.
$$\forall x \forall y, ((f(x) = f(y)) \rightarrow x= y)$$
#### Onto/Surjective
A function $f$ is *onto/surjective* if and only if every element in the *target/codomain* of $f$ is mappeable, meaning that $\text{Range} = \text{Target}/\text{Codomain}$.
$$\forall b \in B, \exists a \in A, (f(a)=b)$$

#### One-to-One Correspondence/Bijection
If a function $f$ is both *onto/surjective* and *one-to-one/injective* then it is called a *bijection*.
### Inverse Function
If $f$ is a function that is also a *bijection*, where $f(a) = b$ then we have $f^{-1}$ which is called the *inverse* of $f$ and $f(b) = a$.
$$f(a) = b \rightarrow f^{-1} (b) =a$$
### Identity Function
An *identity function* is a function that maps its *input* back to *itself*. The identity function is a *bijection*.
$$f : A \rightarrow A \text{  and  } f(a)=a$$