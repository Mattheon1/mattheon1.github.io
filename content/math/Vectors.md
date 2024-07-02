---
---
---
## Why talk about vectors???

Given the topics that will be covered in this guide, it may seem odd to start with what is likely the billionth vector review for most. In truth this is not meant to be a comprehensive lesson on linear-algebra (though I may make that at some point!) but rather a brief refresher meant to do two things:

- 1.) Disambiguate notation that will be commonly used throughout this website (this includes any future projects)

- 2.) Provide what I believe is a unique perspective on some topics that will help to frame later ideas.

With all of that in mind, the first question we should answer is "What is a vector?"

The most concise answer is that a vector $\vec {v}$ is an element of a vector space $\textbf{V}$. In order for a set $\textbf{V}$ to constitute a vector space, there is a list of requirements (called the vector axioms) which must be satisfied which are

$$
\begin{gathered}
\forall (\vec{u},\vec{v},\vec{w}) \in\textbf{R}^n \quad \vec{u}+(\vec{v}+\vec{w})=(\vec{u}+\vec{v})+\vec{w}
\end{gathered}
$$
