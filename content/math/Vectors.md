---
---
---
## Why talk about vectors???

Given the topics that will be covered in this guide, it may seem odd to start with what is likely the billionth vector review for most. In truth this is not meant to be a comprehensive lesson on linear-algebra (though I may make that at some point!) but rather a brief refresher meant to do two things:

- 1.) Disambiguate notation that will be commonly used throughout this website (this includes any future projects)

- 2.) Provide what I believe is a unique perspective on some topics that will help to frame later ideas.

With all of that in mind, the first question we should answer is "What is a vector?"

The most concise answer is that a vector $\vec {u}$ is an element of a vector space $\textbf{V}$. In order for a set $\textbf{V}$ to constitute a vector space, there is a list of requirements (called the vector axioms) that must be satisfied:

---

$$
\begin{gathered}
\forall \{\vec{u},\vec{v},\vec{w}\}\in\textbf{V},
\end{gathered}
$$


- 1.)$\quad\vec{u}+(\vec{v}+\vec{w})=(\vec{u}+\vec{v})+\vec{w}$

- 2.)$\quad\vec{u}+\vec{v}=\vec{v}+\vec{u}$

- 3.)$\quad\exists!{\vec{0}}\in\textbf{V} \,s.t. \quad\vec{0}+\vec{u}=\vec{u}$

- 4.)$\quad\exists!(−{\vec{u}})\in\textbf{V} \,s.t. \quad(−\vec{u})+\vec{u}=\vec{0}$

- 5.)$\quad a(b\vec{u})=(ab)\vec{u}$


- 6.)$1\vec{u}=\vec{u}$

- 7.)$(a+b)(\vec{u}+\vec{v})=(a+b)\vec{u}+(a+b)\vec{v}=a(\vec{u}+\vec{v})+b(\vec{u}+\vec{v})=a\vec{u}+b\vec{u}+a\vec{v}+b\vec{v}$

($\forall$  means for all, $\exists!$ means there exists only one, and $\in$ means within)

---

The definition I've given is broad and includes sets such as the set of nth degree polynomials or even $\{0\}$, however most applications of vectors deal with spaces that can be represented as either n-tuples or columns of numbers (such as $\textbf{R}^n$)

A few other properties and definitions that come from the vector axioms are

