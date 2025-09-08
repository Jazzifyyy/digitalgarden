---
{"dg-publish":true,"permalink":"/6-main-notes/the-solution-of-the-characteristic-polynomial-of-a-matrix-yields-the-eigenvalues/","tags":["linear_algebra","info"]}
---

### Statement

We have $\lambda$ is an eigenvalue of a matrix $A$ iff $\lambda$ is a root of the [[6 - Main Notes/characteristic polynomial of a matrix\|characteristic polynomial]].
### Proof

$$\begin{align}
A\mathbf{v}&=\lambda \mathbf{v} \\
\iff A\mathbf{v}&=\lambda I\mathbf{v} \\
\iff (A-\lambda I)\mathbf{v} &=0 \\
\iff \det(A-\lambda I) &= 0.
\end{align}$$
