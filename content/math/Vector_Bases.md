---
title: Vector Bases and Coordinate Vectors
---

Building upon the concepts of vector spaces, linear combinations, span, and linear independence, we now delve into one of the most useful concepts in linear algebra: the vector basis.

A basis $B_{W}$ is a linearly independent set of vectors (Usually denoted $\{\vec{e}_{1},\cdots,\vec{e}_{n}\}$) that spans a subspace $\textbf{W}$. While a basis can be defined for any subspace, the real reason bases are so powerful can only be seen when we define a basis for an entire space $\textbf{V}$ . 

Given a vector space $\textbf{V}$ and a basis for the space $B_{V} \equiv \{\vec{e}_1,\cdots,\vec{e}_n\}$, we can define the decomposition of any $\vec{u}\in\textbf{V}$ on the basis $B_{V}$ as the unique linear combination 

$$
\begin{gathered}
\sum_{i=1}^n u_{i}\vec{e}_i \,\text{     s.t.     }\, \vec{u}=\sum_{i=1}^n u_{i}\vec{e}_i
\end{gathered}
$$

and we define each $u_i$ to be the components or coordinates of $\vec{u}$ on the basis $B_{V}$

