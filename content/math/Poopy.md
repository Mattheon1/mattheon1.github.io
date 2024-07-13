
---
title: Vector Bases and Coordinate Vectors
---


Building upon our understanding of vector spaces, linear combinations, span, and linear independence, we now turn to one of the most powerful concepts in linear algebra: the vector basis.

A basis $B_{W}$ for a subspace $\textbf{W}$ is a set of vectors that is both linearly independent and spanning for $\textbf{W}$. A vector basis may be defined for any subspace and is not limited to [[https://mathworld.wolfram.com/ProperSubset.html | proper]]subspaces. In fact any set with vector space structure has at minimum one basis. Typically denoted as $\{\vec{e}_{1},\cdots,\vec{e}_{n}\}$, a basis has a crucial property: it's minimal. This means that removing any vector from the basis would result in a set that no longer spans $\textbf{W}$.

This minimality property leads us to a fundamental characteristic of vector spaces: dimension. The dimension of a vector space is defined as the number of vectors in any basis for that space, and is an intrinsic property held by all spaces.

Despite the abstract presentation of these (hopefully familiar) concepts, bases and dimension are two of the most practical ideas in linear algebra due to how they simplify and give meaning to abstract vector operations. Taking advantage of the fact that any vector in a space $\textbf{V}$ is within the span of a basis $B_{V}\equiv \{ \vec{e}_{1},\cdots, \vec{e}_{n}\}$, we can express all vectors $\vec{u}\in\textbf{V}$ as linear combinations 

$$
\begin{gathered}
\vec{u} = \sum_{i=1}^n u_{i}\vec{e}_{i}
\end{gathered}
$$
where each $u_i$ is called a component or coordinate of $\vec{u}$ with respect to the basis $B_{V}$. The utility of this expression is immediately obvious when we try to make sense of the sum of two vectors. Take for example the vector equation $\vec{u} + \vec{v} = \vec{w}$. Without a basis, this equation provides limited information and is little more than a definition. However, when we express these vectors in terms of a basis, the equation becomes:
$$
\begin{gathered}
\vec{u}+ \vec{v} = \left(\sum_{i=1}^{n} u_{i} \vec{e}_{i}\right) + \left(\sum_{j=1}^{n} v_{j} \vec{e}_{j}\right) = \sum_{i=1}^{n} (u_{i}+v_{i}) \vec{e}_{i} = \sum_{i=1}^{n} w_{i} \vec{e}_{i} = \vec{w} 
\end{gathered}
$$
This representation allows us to compute the components of $\vec{w}$ directly from those of $\vec{u}$ and $\vec{v}$, and to identify relationships between vectors that might not be apparent in their abstract form.
For instance, consider the case where $\vec{u} = \vec{e}_{1} + \vec{e}_{2}$ and $\vec{v} = 2\vec{e}_{1} + 2\vec{e}_{2}$ for the previous equation. In this basis representation, we can immediately see that $\vec{v} = 2\vec{u}$ (and thus $\vec{w} = 3 \vec{u} $).

This
