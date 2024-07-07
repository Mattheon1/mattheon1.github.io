
---
title: Linear Combinations
---


The vector axioms define the properties of scalar multiplication and vector addition, but often we'll seek to make use of both operations at once. This leads us to the more general concept of a linear combination.

A linear combination of vectors is simply just a sum of vectors weighted by scalar coefficients. Given any indexable set of vectors $S\equiv \{\vec{u}_1,\cdots,\vec{u}_n\}$ within a space $\textbf{V}$ we can compactly represent any linear combination of vectors within this set like: 

$$
\begin{gathered}
\displaystyle\sum_{i=1}^{n}c_{i}\vec{u}_i=c_1\vec{u}_1+...+c_n\vec{u}_n
\end{gathered}
$$


Where each coefficient could be any arbitrary scalar. Also take note that since $\textbf{V}$ is closed under both addition and multiplication, a linear combination of vectors is itself a vector. There isn't much added benefit that comes from discussing specific linear combinations of vectors, as they are already fully described by the vector axioms. The main benefit comes from the ability to construct the set of all linear combinations of a given set $S$, which we call the span.

Formally the span of a subset $S$ of a vector space $\textbf{V}$ over a  [[https://en.wikipedia.org/wiki/Field_(mathematics)|Field]] ${\textbf{F}}$ can be defined as:

$$
\begin{gathered}
span(S)= \left\{
\sum_{i=1}^{n}c_{i}\vec{u}_{i} \,\middle|\, c_{i}\in\mathbf{F},\vec{u}_i\in S
\right\}
\end{gathered}
$$

The span of a set of vectors is special as far as subsets of $\textbf{V}$ go in that it can be demonstrated to have its own vector space structure. All axioms dealing with the properties of operations are automatically met as a subset of a $\textbf{V}$, and the remaining two axioms (existence of additive inverse and identity) can be shown to be satisfied in the following ways:

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

The span of a set of vectors is not unique however. For example, take two sets in $\textbf{V}$:

$$
\begin{gathered}
S_{1}\equiv\{\vec{u}_{1},\cdots,\vec{u}_{n}\} \text{ and } S_{2}\equiv\{\vec{u}_{1},\cdots,\vec{u}_n+\vec{u}_1\}. \\[1em]
span(S_{1})= \left\{\displaystyle\sum_{i=1}^nc_{i}\vec{u}_{i}\middle|c_{i}\in\textbf{F}\right\}, \\[1em]
span(S_{2})= \left\{\left(\displaystyle\sum_{i=1}^{n-1}c_{i}\vec{u}_{i}\right)+c_n\left(\vec{u}_{n}+\vec{u}_{1}\right)\middle|c_{i}, c_{n}\in\textbf{F}\right\}
\end{gathered}
$$

We can pretty easily see that the span of both sets should be the same, as we could redefine $c_{1}\equiv c_{1}+c_{n}$ (since the coefficients $c_i$   are arbitrary) and construct the span of both sets in exactly the same form.

Similarly for a triplet of sets:

$$
\begin{gathered}
S_{1} \equiv \{\vec{u}_{1} \cdots, \vec{u}_{n}\}, \,
S_{2} \equiv \left\{\sum_{i=1}^n b_{i}\vec{u}_i\right\}, \text{ and }
S_{3} \equiv S_{1} \cup S_{2},
\end{gathered}
$$

being a member of the union of two sets means an element is within either set, or tthe intersection of both. A vector being within the span of the union of two sets means the vector is a linear combination of members of either set, or both sets. Thus we can represent the spans of $S_{1}$ and the union $S_{1}\cup S_{2} like

$$
\begin{gathered}
span(S_{1})= \left\{\displaystyle\sum_{i=1}^nc_{i}\vec{u}_{i}\middle|c_{i}\in\textbf{F}\right\}, \\[1em]\\
span(S_{3})= \left\{\left(\displaystyle\sum_{i=1}^{n}a_{i}\vec{u}_{i}\right)+c\left(\displaystyle\sum_{i=1}^{n}b_{i}\vec{u}_{i}\right)\middle|a_{i},b_{i},c\in\textbf{F}\right\}.
\end{gathered}
$$ 

Like we had in the previous example we can combine both sums in the definition of $span(S_{3})$ by redefining $a_{i}+c(b_{i})\equiv c_{i}$. Doing so reduces the two sums into one and we can see both $S_{1}$ and $S_{3}$ have the same span.

The first and second examples illustrate an important concept: the subspace spanned by a set of vectors is not unique. However, there is a crucial distinction between the two scenarios:

- In the first example, we have two sets with the same number of elements that span the same subspace. This demonstrates that different sets can generate the same span.
- The second example involves adding a new element to an existing set without changing the span. This shows that adding certain elements to a set may not expand the subspace it generates.

This distinction leads us to a fundamental property of sets of vectors known as [[linear_independence|linear independence]].


