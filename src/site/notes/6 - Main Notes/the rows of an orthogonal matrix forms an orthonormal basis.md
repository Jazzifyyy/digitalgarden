---
{"dg-publish":true,"permalink":"/6-main-notes/the-rows-of-an-orthogonal-matrix-forms-an-orthonormal-basis/","tags":["linear_algebra","info"]}
---

### Statement

The matrix $A$ is an [[6 - Main Notes/orthogonal matrix\|orthogonal matrix]] in $\mathbb{M}_{n}(\mathbb{R})$ iff its rows $c_{1},\dots,c_{n}$ are orthonormal. 
### Proof

$$\begin{align}
A^TA \text{ is orthogonal}&\iff c_{i} \cdot c_{j}=0 \text{ for }i \neq j \text{ and }c_{i}\cdot c_{j}=1 \text{ for }i=j  \\
&\iff \{ c_{1},\dots,c_{n} \}\text{ is orthonormal basis}.
\end{align}$$
Note that $\{ c_{1} \}$