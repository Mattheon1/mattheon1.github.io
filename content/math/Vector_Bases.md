---
title: Vector Bases and Coordinate Vectors
---

Building upon the concepts of vector spaces, linear combinations, span, and linear independence, we now delve into one of the most useful concepts in linear algebra: the vector basis.

A basis $B_{W}$ is a linearly independent set of vectors (Usually denoted $\{\vec{e}_{1},\cdots,\vec{e}_{n}\}$) that spans a subspace $\textbf{W}$. While a basis can be defined for any subspace, the real reason bases are so powerful can only be seen when we define a basis for an entire space $\textbf{V}$ . 

Given a vector space $\textbf{V}$ and a basis for the space $B_{V} \equiv \{\vec{e}_1,\cdots,\vec{e}_n\}$, we can define the decomposition of any vector $\vec{u}\in\textbf{V}$ on the basis $B_{V}$ as the unique linear combination 

$$
\begin{gathered}
\sum_{i=1}^n u_{i}\vec{e}_i \,\text{     s.t.     }\, \vec{u}=\sum_{i=1}^n u_{i}\vec{e}_i
\end{gathered}
$$

and we define each $u_i$ to be the components or coordinates of $\vec{u}$ on the basis $B_{V}$. The advantage of defining vectors in terms of their components on a basis is that we gain the ability to conceptualize how different vectors in a space relate to eachother.

Take two vectors $ \vec{u}$ and $\vec{v}$ which sum to a third vector $\vec{w}$. Without a basis the statement $ \vec{u}+ \vec{v} = \vec{w}\,$ is no more than a definition. The only thing we know about $ \vec{v}$ and $ \vec{u}$ is that they sum to $ \vec{w}$, and we could equally view this equation as a definition for $ \vec{u}$ or $ \vec{v}$.

If we instead represent both $\vec{u}$ and $\vec{v}$ as linear combinations of the basis vectors, then the sum $ \vec{u}+ \vec{v}$ may be written as   

$$
\begin{gathered}
\vec{u}+ \vec{v} =  \sum_{i=1}^{n} u_{i} \vec{e}_{i} + \sum_{j=1}^{n} v_{j} \vec{e}_{j} = \sum_{i=1}^{n} (u_{i}+v_{i}) \vec{e}_{i} = \sum_{i=1}^{n} w_{i} \vec{e}_{i} = \vec{w}  \,.
\end{gathered}
$$

If we know the components of $\vec{u}$ and $\vec{v}$ then we also know the components of $\vec{w}$ and can define $\vec{w}$ in terms of the basis instead.

This may seem like an unimportant difference since ultimately we're still defining $\vec{w}$ in terms of $\vec{u}$ and $\vec{v}$, but we've gained the ability to make statements about the characteristics of that definition.

If $\vec{u}$ was $ \vec{e}_{1}+ \vec{e}_{2}\,$, and $\vec{v}$ was $ 2 \vec{e}_{1} + 2\vec{e}_{2}$, the despite never having defined $\vec{v}$ in terms of $\vec{u}$, we can see $\vec{v} = 2\vec{u} $  
