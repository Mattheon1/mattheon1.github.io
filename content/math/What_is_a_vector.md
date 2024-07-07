
---
title:  What is a Vector?
---
The most concise answer is that a vector $\vec {u}$ is an element of a vector space $\textbf{V}$. In order for a set $\textbf{V}$ to constitute a vector space, we require the existence of two operations on elements of $\textbf{V}$ known as vector addition and scalar multiplication. These operations must be defined in a way which is compatible with a set of requirements (called the vector axioms) that define the structure of a vector space. The vector axioms can be expressed in the following concise form:



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

---
This definition is rather dense and includes sets not commonly thought of as vector spaces (such as the set of nth degree polynomials or even $\{0\}$). Luckily most of these requirements are things we tend to take for granted (like associativity) and so we wont have to reference them too much. We'll also mostly be focusing on [[https://en.wikipedia.org/wiki/Euclidean_vector|Euclidean vector spaces]] and that comes with a lot of geometric intuition that we can leverage.

The vector axioms define how to add vectors and multiply them by scalars, but a general framework for how to contruct new vectors by combining both of these operations is going to be helpful moving forward. Thus we must introduce the concept of a [[Linear_combinations|Linear Combination]].

