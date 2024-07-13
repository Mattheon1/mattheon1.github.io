---
title: Linear Independence
---

A linearly independent set $A\equiv\{\vec{u}_1,\cdots,\vec{u}_n\}$ has the property that no element in $A$ is a linear combination of any other elements (or lies within the span of the other elements). Symbolically this means 

$$
\begin{gathered}
\forall \vec{u}_{i}\in A,\,\, \vec{u}_{i}\notin span(A\backslash\{\vec{u}_{i}\}).
\end{gathered}
$$

Unrusprisingly, the complement to linear independence is known as linear dependence. A linearly dependent set of vectors contains elements which can be expressed as linear combinations of other elements in the set. Its important to note that no single element of a linearly dependent set is dependent, but rather they all are. This is because if we have a dependent set  $B\equiv\{\vec{v}_1,\cdots,\vec{v}_n\}$ and an equation expressing any one vector in $B$ like

$$
\begin{gathered}
\vec{v}_{i}=\sum_{j\neq{i}}^{n}c_{j}\vec{v}_{j} \,
\end{gathered}
$$

then we can express some other vector in $B$ as a linear combinations of the other elements by first subtracting $\vec{v}_{i}$ from both sides to get the zero vector

$$
\begin{gathered}
\vec{0}= \left(\sum_{j\neq{i}}^{n}c_{j}\vec{v}_{j} \right) -\vec{v}_{i}
\end{gathered}
$$

defining $c_{i}\equiv -1$ to include $-\vec{v}_i$ in the sum [^1]

$$
\begin{gathered}
\vec{0}= \sum_{j=1}^{n}c_{j}\vec{v}_{j}
\end{gathered}
$$

subtracting from both sides some $c_{k}\vec{v}_k$ (with $c_{k}\ne 0$)

$$
\begin{gathered}
(-c_{k})\vec{v}_k = \sum_{j\neq{k}}^{n} c_j \vec{v}_j
\end{gathered}
$$



and finally multiplying both sides by $-\frac{1}{c_{k}}$ to get

$$
\begin{gathered}
\vec{v}_k = \left(-\frac{1}{c_k}\right)\sum_{j \neq k}^{n} c_j \vec{v}_j =\sum_{j\neq{k}}^n \left(-\frac{c_{j}}{c_{k}}\right)\vec{v}_j
\end{gathered}
$$

which is an equation expressing $\vec{v}_k$ in terms of a linear combination of other vectors in $B$, making $\vec{v}_k$ also a dependent element.

---
One important fact regarding span and linear independence is that if you consider all possible spanning sets for a given subspace $\textbf{W}$ and focus on the ones with the smallest number of vectors, you'll discover that each of these minimal spanning is linearly independent, and that all linearly independent spanning sets are minimal.

While we won't prove this claim outright here, we can provide some justification by examining the implications of the existence of a set $S\equiv\{\vec{u}_1,\cdots,\vec{u}_n\}$ that is both a minimal spanning set and linearly dependent.

If $S$ were dependent, then we could express any one of the elements $\vec{u}_i$ as a linear combination of the others, as follows:

$$
\begin{gathered}
\vec{u}_i = \sum_{j\neq {i}}^{n} c_{j}\vec{v}_{j}\,\,.
\end{gathered}
$$

Removing the element $\vec{u}_i$ from $S$ would not alter the span of the set since any vector within $span(S)$ that is expressed in terms of $\vec{u}_i$ could instead be expressed using the other vectors in the set.

The set $S\backslash\{\vec{u_{i}}\}$ (which is just $S$ excluding $\vec{u}_i$) is smaller than $S$ but has the same span, and thus $S$ could not have been a minimal spanning set.
Since we can repeat this process until we are left with a linearly independent set, all minimal spanning sets must be linearly independent.

This relationship between an independent spanning set and the space it spans brings us to one of the most important and powerful constructions in linear algebra (which will also be the last two topic we'll cover before getting to [[Euclidean_spaces|Euclidean vector spaces]]), [[Vector_Bases|basis vectors and coordinate spaces]].






[^1]: As an aside, this line provides us an alternative definition of linear dependence, which is that for any linearly dependent set $\\B\equiv\{\vec{v}_1,\cdots,\vec{v}_n\},\,\,\exists \displaystyle\sum_{i=1}^n c_{i}\vec{v}_{i}$ with not all $c_{i}=0 \text{ s.t. } \displaystyle\sum_{i=1}^n c_{i}\vec{v}_{i} = \vec{0}$

