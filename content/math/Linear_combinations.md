---
title: Linear Combinations
---


The vector axioms define the properties of scalar multiplcation and vector addition, but often we'll seek to make use of both operations at once. This leads us to the more general concept of a linear combination.

A linear combination of vectors is simply just a sum of vectors weighted by scalar coefficients. Given any indexable set of vectors $S\equiv \{\vec{u}_1,\cdots,\vec{u}_n\}$ within a space $\textbf{V}$ we can compactly represent any linear combination of vectors within this set like: 

$$
\begin{gathered}
\displaystyle\sum_{i=1}^{n}c_{i}\vec{u}_i=c_1\vec{u}_1+...+c_n\vec{u}_n
\end{gathered}
$$


Where each coefficient could be any arbitray scalar. Also take not that since $\textbf{V}$ is closed under both addition and multiplication, a linear combination of vectors is itself a vector. There isn't much added benefit that comes from discussing specific linear combinations of vectors, as they are already fully described by the vector axioms. The main benefit of defining a linear combination as we have is the ability to construct the set of all linear combinations of a given set $S$, which we call the span.

Formally the span of a subset $S$ of a vector space $\textbf{V}$ over a  [[https://en.wikipedia.org/wiki/Field_(mathematics)|Field]] ${\textbf{F}}$ can be defined as:

$$
\begin{gathered}
span(S)= \left\{
\sum_{i=1}^{n}c_{i}\vec{u}_{i} \,\middle|\, c_{i}\in\mathbf{F},\vec{u}_i\in S
\right\}
\end{gathered}
$$

The span of a set of vectors is special as far as subsets of $\textbf{V}$ go in that it can be demonstrated to have its own vector space strucutre. All axioms dealing with the properties of operations are automatically met as a subset of a $\textbf{V}$, and the remaining two axioms (existence of additive inverse and identity) can be shown to be satisfied in the following ways:

#### Additive Inverse

$$
\begin{gathered}
let \,\sum_{i=1}^nc_{i}\vec{u}_{i}\equiv\vec{v}. \\ \\\forall\vec{v}\in span(S),\\\\ -\vec{v}=-\left(\sum_{i=1}^nc_{i}\vec{u}_{i}\right) =\sum_{i=1}^n(-c_{i})\vec{u}_{i}\,,\\\\ \sum_{i=1}^n(-c_{i})\vec{u}_{i}\in span(S)
\end{gathered}
$$

#### Additive identity

$$
\begin{gathered}
\vec{0}=\sum_{i=1}^n\vec{0}=\sum_{i=1}^n0\vec{u}_{i}\, ,\\\\\sum_{i=1}^{n}0\vec{u}_{i}\in span(S)
\end{gathered}
$$

Thus given any set of vectors in $\textbf{V}$, the span of the set is simultaneously a subset of $\textbf{V}$ and a   vector space of its own. All such subsets are referred to as subspaces and are generally assumed to be subsets of larger vector spaces (though all vectors spaces are technically subspaces of themselves)

The span of a set of vectors is not unique however. For example, take two sets in $\textbf{V}$,

$$
\begin{gathered}
S_{1}\equiv\{\vec{u}_{1},\cdots,\vec{u}_{n}\} \text{ and } S_{2}\equiv\{\vec{u}_{1},\cdots,\vec{u}_n+\vec{u}_1\}. \\[1em]
span(S_{1})= \left\{\displaystyle\sum_{i=1}^nc_{i}\vec{u}_{i}\middle|c_{i}\in\textbf{F}\right\}, \\[1em]
span(S_{2})= \left\{\left(\displaystyle\sum_{i=1}^{n-1}c_{i}\vec{u}_{i}\right)+c_n\left(\vec{u}_{n}+\vec{u}_{1}\right)\middle|c_{i}, c_{n}\in\textbf{F}\right\}
\end{gathered}
$$

We can pretty easily see that the span of both sets should be the same, as we could redefine $c_{1}\equiv c_{1}+c_{n}$ (since the coefficients $c_i$   are arbitrary) and construct the span of both sets in exactly the same form.

Similarly for a triplet of sets

$$
\begin{gathered}
S_{1} \equiv \{\vec{u}_{1} \cdots, \vec{u}_{n}\}, \,
S_{2} \equiv \left\{\sum_{i=1}^n b_{i}\vec{u}_i\right\}, \text{ and }
S_{3} \equiv S_{1} \cup S_{2}
\end{gathered}
$$

$$
\begin{gathered}
span(S_{1})= \left\{\displaystyle\sum_{i=1}^nc_{i}\vec{u}_{i}\middle|c_{i}\in\textbf{F}\right\}, \\[1em]\\
span(S_{3})= \left\{\left(\displaystyle\sum_{i=1}^{n}a_{i}\vec{u}_{i}\right)+c\left(\displaystyle\sum_{j=1}^{n}b_{j}\vec{u}_{j}\right)\middle|a_{i},b_{j},c\in\textbf{F}\right\}.
\end{gathered}
$$ 

Like we had in the previous example we can combine both sums in the definition of $span(S_{3})$ by using the same index and redefining $a_{i}+c(b_{i})\equiv c_{i}$. Doing so we can see that once again both $S_{1}$ and $S_{3}$ have the same span.

The first and second examples illustrate an important concept: the subspace spanned by a set of vectors is not unique. However, there is a crucial distinction between the two scenarios:

- In the first example, we have two sets with the same number of elements that span the same subspace. This demonstrates that different sets can generate the same span.
- The second example involves adding a new element to an existing set without changing the span. This shows that adding certain elements to a set may not expand the subspace it generates.

This distinction leads us to a fundamental property of sets of vectors known as linear independence.

---
Linear Independence
---

A linearly independent set $A\equiv\{\vec{u}_1,\cdots,\vec{u}_n\}$ has the property that no element in $A$ is a linear combination of any other elements (or lies within the span of the other elements). Symbolically this means 

$$
\begin{gathered}
\forall \vec{u}_{i}\in A,\,\, \vec{u}_{i}\notin span(A\backslash\{\vec{u}_{i}\}).
\end{gathered}
$$

Predictably, the complement to linear independence is known as linear dependence. A linearly dependent set of vectors contains elements which can be expressed as linear combinations of other elements in the set. Important to note is that no single element of a linearly dependent set is dependent, but rather they all are. This is because if we have a dependent set  $B\equiv\{\vec{v}_1,\cdots,\vec{v}_n\}$ and an equation expressing any one vector in $B$ like

$$
\begin{gathered}
\vec{v}_{i}=\sum_{j\neq{i}}^{n}c_{j}\vec{v}_{j} \,,
\end{gathered}
$$

then we can express some other vector in $B$ as a linear combinations of the other elements by first subtracting $\vec{v}_{i}$ from both sides to get the zero vector

$$
\begin{gathered}
\vec{0}= \left(\sum_{j\neq{i}}^{n}c_{j}\vec{v}_{j} \right) -\vec{v}_{i}
\end{gathered}
$$

and then subtracting from both sides some $c_{k}\vec{v}_k$ (with $c_{k}\ne 0$)

$$
\begin{gathered}
(-c_{k})\vec{v}_k = \left(\sum_{\substack{j\neq{i} \\ j \neq k}}^{n} c_j \vec{v}_j\right) - \vec{v}_i
\end{gathered}
$$

and finally multiplying both sides by $-\frac{1}{c_{k}}$ to get

$$
\begin{gathered}
\vec{v}_k = -\frac{1}{c_k} \left(\left(\sum_{\substack{j\neq{i} \\ j \neq k}}^{n} c_j \vec{v}_j\right) - \vec{v}_i\right).
\end{gathered}
$$
