---
title: Linear Combinations
---


The vector axioms define the properties of scalar multiplcation and vector addition, but often we'll seek to make use of both operations at once. This leads us to the more general concept of a linear combination.

A linear combination of vectors is simply just a sum of vectors weighted by scalar coefficients. Given any indexable set of vectors from $\textbf{V}$ $\{\vec{u}_1,...,\vec{u}_n\}$ (denoted $S$) we can compactly represent any linear combination of vectors within this set like: 

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
