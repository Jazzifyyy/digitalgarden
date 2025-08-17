---
{"dg-publish":true,"permalink":"/6-main-notes/theta-notation/","tags":["dsa","info"]}
---

### Definition

Given two functions $f$ and $g$, we say that $f(n) \in \Theta(g(n))$ iff there exists constants $c_{1},c_{2},n_{0}>0$ such that $$c_{1}g(n)\leq f(n)\leq c_{2}g(n)$$ for all $n>n_{0}$.

Note that this is equivalent to
$$\Theta(g)= O(g) \cap \Omega(g).$$
(See: [[6 - Main Notes/Big-o notation\|Big-o notation]], [[6 - Main Notes/Big-omega notation\|Big-omega notation]])