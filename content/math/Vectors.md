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


If you want to go ahead with the quickest vector review of all time, then the first question we should ask ourselves is, [[What_is_a_vector|What is a vector?]]

---
## Linear Independence and Vector Bases
For any subspace $\textbf{W}$ of a vector space $\textbf{V}$, there are infinitely many choices of spanning sets $S \,\,s.t. \,span(S)=\textbf{W}$. 

This is because the addition of a linear combination of vectors already in $S$ doesn't change the span of $S$, but still results in a completely new spanning set. Adding linear combinations of elements to current elements results in a new set that has the same span as well. 

$$
\begin{gathered}
\text{span} \left\{
\vec{u}_1,\ldots,\vec{u}_n
\right\} = \text{span}\left\{\vec{u}_1,\ldots,\vec{u}_n,\sum_{i=1}^nc_{i}\vec{u}_i
\right\}=span\left\{\vec{u}_1+\sum_{i=1}^nc_{i}\vec{u}_i,\ldots,\vec{u}_n+\sum_{i=1}^nc_{j}\vec{u}_j
\right\}
\end{gathered}
$$

While there is no way to bound the number of sets that span the same subspace, we can place a limit on the minimum size.

Given a set S = \{\vec{u}_1,...\vec{u}_n\}$
 

## Coordinate Bases for Euclidian Vector Spaces 
