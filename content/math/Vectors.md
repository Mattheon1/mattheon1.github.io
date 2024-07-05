---
---
---
## Why talk about vectors???

Given the complexity of some of the topics that will be covered in this guide, it may seem odd to start with what is likely the billionth vector review for most. While annoying for some, you can rest easy knowing this section is not intended to be a comprehensive lesson on linear-algebra, and in fact will seem blazingly quick for someone with little to no prior knowledge bout vector spaces (if you have no idea what a vector is, you might find [[https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab|this series helpful]]).

Instead, the first part of this page (which serves as the boiler-plate review) serves two purposes:


- 1.) Disambiguate notation that will be commonly used throughout this website (this includes any future projects)

- 2.) Provide a smooth transition into the latter half of this page, which will most likely be new material for some.

From the second half onward, it will be assumed that you at least know what a vector is and some basic facts about vector spaces and operations on vector spaces.

If you feel super confident in your knowledge and feel the first section would be a waste of time, [click here](#coordinate-bases-for-euclidian-vector-spaces).


If you want to go ahead with the quickest vector review of all time, then the first question we should ask ourselves is:

---
## What is a Vector?

The most concise answer is that a vector $\vec {u}$ is an element of a vector space $\textbf{V}$. In order for a set $\textbf{V}$ to constitute a vector space, there is a list of requirements (called the vector axioms) that must be satisfied:

---

$$
\begin{gathered}
\forall \{\vec{u},\vec{v},\vec{w}\}\in\textbf{V},
\end{gathered}
$$

- 1.)$\quad\vec{u}+\vec{v}\in\textbf{V}$,$\quad a\vec{u}\in\textbf{V}$   |   (Closure under vector addition and scalar multiplication)

- 2.)$\quad\vec{u}+(\vec{v}+\vec{w})=(\vec{u}+\vec{v})+\vec{w}$   |   (associativity of addition)

- 3.)$\quad\vec{u}+\vec{v}=\vec{v}+\vec{u}$   |   (commutativity of addition)

- 4.)$\quad\exists!{\vec{0}}\in\textbf{V} \,s.t. \quad\vec{0}+\vec{u}=\vec{u}$   |   (existence of additive identity)

- 5.)$\quad\exists!(−{\vec{u}})\in\textbf{V} \,s.t. \quad(−\vec{u})+\vec{u}=\vec{0}$   |   (existence of additive inverse)

- 6.)$\quad a(b\vec{u})=(ab)\vec{u}$   |   (scalar multiplication is equivalent to [[https://en.wikipedia.org/wiki/Field_(mathematics)|Field]] multiplcation)


- 7.)$\quad1\vec{u}=\vec{u}$   |   (multiplication by the identity element returns the vector original vector)

- 8.)$\quad(a+b)(\vec{u}+\vec{v})=(a+b)\vec{u}+(a+b)\vec{v}=a(\vec{u}+\vec{v})+b(\vec{u}+\vec{v})=a\vec{u}+b\vec{u}+a\vec{v}+b\vec{v}$   |   (scalar multiplication distributes)

($\forall$  means for all, $\exists!$ means there exists only one, and $\in$ means within)

This definition is rather dense and includes sets not commonly thought of as vector spaces (such as the set of nth degree polynomials or even $\{0\}$), however for the majority of this section we wont need to reference it and will tend to focus on what most people imagine when thinking of a vector space, [[https://en.wikipedia.org/wiki/Euclidean_vector|Euclidean vector spaces]] .

---
## Linear Combinations and span

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

---
## Linear Independence and Vector Bases
For any subspace $\textbf{W}$ of a vector space $\textbf{V}$, there are infinitely many choices of spanning sets $S \,\,s.t. \,span(S)=\textbf{W}$.

This can be easily shown as 

$$
\begin{gathered}
\text{span}({\vec{u}_1,...,\vec{u}_n})
\end{gathered}
$$

While there is no way to bound the number of sets that span the same subspace, we can place a limit on the minimum size.

Given a set S = \{\vec{u}_1,...\vec{u}_n\}$
#### 

## Coordinate Bases for Euclidian Vector Spaces 
