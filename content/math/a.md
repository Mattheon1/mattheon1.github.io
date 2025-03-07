---
title: Vector Bases and Coordinate Vectors
---


Building upon our understanding of vector spaces, linear combinations, span, and linear independence, we now turn to one of the most powerful concepts in linear algebra: the vector basis.

A basis $B_{W}$ for a subspace $\textbf{W}$ is a set of vectors that is both linearly independent and spanning for $\textbf{W}$. A vector basis may be defined for any subspace and is not limited to [[https://mathworld.wolfram.com/ProperSubset.html | proper]]subspaces. In fact any set with vector space structure has at minimum one basis. Typically denoted as $\{\vec{e}_{1},\cdots,\vec{e}_{n}\}$, a basis has a crucial property: it's minimal. This means that removing any vector from the basis would result in a set that no longer spans $\textbf{W}$.

This minimality property leads us to a fundamental characteristic of vector spaces: dimension. The dimension of a vector space is defined as the number of vectors in any basis for that space, and is an intrinsic property held by all spaces.

Despite their abstract nature, bases and dimension are two of the most practical ideas in linear algebra, as they simplify and give meaning to abstract vector operations. The power of these concepts lies in their ability to represent any vector in a space using a finite set of numbers.
Since a basis for a space $\textbf{V}$ spans the entire space, any vector in $\textbf{V}$ is within the span and may be expressed as a linear combination of the basis vectors, which is guaranteed to be unique. Specifically, given a basis $B_{V}\equiv \{ \vec{e}_{1},\cdots, \vec{e}_{n}\}$, we can express all vectors $\vec{u}\in\textbf{V}$ as:
$$
\begin{gathered}
\vec{u} = \sum_{i=1}^n u_{i}\vec{e}_{i}
\end{gathered}
$$
where each $u_i$ is called a component or coordinate of $\vec{u}$ with respect to the basis $B_{V}$. Importantly, the number of these coordinates is always equal to the dimension of the space.


The utility of this expression is immediately obvious when we try to make sense of the sum of two vectors. Take for example the vector equation $\vec{u} + \vec{v} = \vec{w}$. Without a basis, this equation provides limited information and is little more than a definition. However, when we express these vectors in terms of a basis, the equation becomes:
$$
\begin{gathered}
\vec{u}+ \vec{v} = \left(\sum_{i=1}^{n} u_{i} \vec{e}_{i}\right) + \left(\sum_{j=1}^{n} v_{j} \vec{e}_{j}\right) = \sum_{i=1}^{n} (u_{i}+v_{i}) \vec{e}_{i} = \sum_{i=1}^{n} w_{i} \vec{e}_{i} = \vec{w} 
\end{gathered}
$$
This representation allows us to compute the components of $\vec{w}$ directly from those of $\vec{u}$ and $\vec{v}$, and to identify relationships between vectors that might not be apparent in their abstract form.

For instance, consider the case where $\vec{u} = \vec{e}_{1} + \vec{e}_{2}$ and $\vec{v} = 2\vec{e}_{1} + 2\vec{e}_{2}$ for the previous equation. Despite having never defined $\vec{v}$ in terms of $\vec{u}$, by looking at the coordinates of the vectors we can immediately see that $\vec{v} = 2\vec{u}$ (and thus $\vec{w} = 3 \vec{u} $).

---

The utility of basis representations is so widely recognized that many people often equate the coordinates on a basis with the vector itself. While they are technically distinct, if we fix a basis for a vector space $\textbf{V}$, we can establish a rigorous mathematical relationship between a vector and its coordinates that justifies this intuition.

In a finite n-dimensional vector space $\textbf{V}$ with a basis $B_{V} \equiv \{\vec{e}_1, \cdots, \vec{e}_n\}$, we already know we can express a vector $\vec{u}$ as 

$$
\begin{gathered}
\sum_{i=1}^{n} u_{i} \vec{e}_{i} 
\end{gathered}
$$

However if we make the choice to perform all calculations in a specified basis, we don't need to explicitly show the basis vectors. Instead it can be understood that for a vector $\vec{u}$, the coordinate $u_{i}$ corresponds to $\vec{e}_{i}$  and we could represent $\vec{u}$ with the ordered n-tuple $(u_{1}.\cdots,u_{n})$ or column matrix: 

$$
\begin{bmatrix}
u_{1}\\
\vdots \\
u_{n}
\end{bmatrix} 
$$

instead. This n-tuple (or column matrix) is known as the coordinate-vector representation of $\vec{u}$ in a given basis, and is actually a member of it's own distinct vector space over the same field $\textbf{F}$ as $\textbf{V}$ known as $\textbf{F}^n$ ($\textbf{R}^n$ or $\textbf{C}^n$ usually).

When we say that there is rigorous justification for the intuition that the coordinate vector space $\textbf{F}^n$ and $\textbf{V}$ are essentially the same, we're referring to a fundamental concept in linear algebra: isomorphism.
An isomorphism is a way of saying that two mathematical objects have the same structure, even if they appear different on the surface. In the context of vector spaces, two spaces are isomorphic if there's a way to transform vectors from one space to the other while preserving all vector operations (like addition and scalar multiplication).
More formally, in linear algebra, if there exists a bijective linear map $f: \textbf{V} \to \textbf{W}$ (that is, a one-to-one and onto linear transformation), then $f$ is an isomorphism and we say $\textbf{V} \cong \textbf{W}$ (the two are isomorphic). A key fact is that two finite-dimensional vector spaces are isomorphic if and only if they have the same dimension.
In our case, the map that takes a vector in $\textbf{V}$ to its coordinate representation in $\textbf{F}^n$ is indeed an isomorphism. This isomorphism allows us to transition seamlessly between the abstract vector space $\textbf{V}$ and the concrete numerical computations in $\textbf{F}^n$, justifying our intuition about working with coordinate vectors.

