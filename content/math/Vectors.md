---
---
---
## Why talk about vectors???

Given the topics that will be covered in this guide, it may seem odd to start with what is likely the billionth vector review for most. In truth this is not meant to be a comprehensive lesson on linear-algebra (though I may make that at some point!) but rather a brief refresher meant to do three things:

- 1.) Disambiguate notation that will be commonly used throughout this website (this includes any future projects)

- 2.) Provide what I believe is a unique perspective on some topics that will help to frame later ideas.

- 3.) Qucikly refamiliarize anyone who might not remember some concepts from linear

With that out of the way, the first question we should answer is "What is a vector?"

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

A linear combination of vectors is simply just a sum of vectors weighted by scalar coefficients. Given any indexable set of vectors from $\textbf{V}$ $\{\vec{u}_1,...,\vec{u}_n\}$ we can compactly represent any linear combination of vectors within this set like: 

$$
\begin{gathered}
\displaystyle\sum_{i=1}^{n}c_{i}\vec{u}_i=c_1\vec{u}_1+...+c_n\vec{u}_n
\end{gathered}
$$


Where each coefficient could be any arbitray scalar. Also take not that since $\textbf{V}$ is closed under both addition and multiplication, a linear combination of vectors is itself a vector. Because generality is usually rewarded in mathematics, it's often more fruitful to consider the set of all possible linear combinations of a given set of vectors. Exploring this idea further brings us to the concept of span.

Formally the span of a set of vectors $S$ within a space $\textbf{V}$ over a  [[https://en.wikipedia.org/wiki/Field_(mathematics)|Field]] ${\textbf{F}}$ can be defined as:

$$
\begin{gathered}
span(S)= \left\{
\sum_{i=1}^{n}c_{i}\vec{u}_{i} \,\middle|\, c_{i}\in\mathbf{F},\vec{u}_i\in S
\right\}
\end{gathered}
$$







