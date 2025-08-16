---
{"dg-publish":true,"permalink":"/6-main-notes/little-o-notation/","tags":["dsa","info"]}
---

### Definition

Given two functions $f$ and $g$, we say that $f \in o(g)$ if for every $\varepsilon>0$, there exists $n_{0}>0$ such that
$$f(n)\leq \varepsilon g(n)$$
for all $n>n_{0}$.

### Note

Note that the little-o notation makes a stronger statement than the corresponding [[6 - Main Notes/Big-o notation\|big-0 notation]].