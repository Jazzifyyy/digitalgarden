---
{"dg-publish":true,"permalink":"/6-main-notes/the-dot-product-of-two-eigenvectors-with-distinct-eigenvalues-of-a-symmetric-matrix-is-zero/","tags":["linear_algebra","info"]}
---

### Statement

Suppose $A$ is a real symmetric matrix and suppose $x_{1},x_{2}$ are the [[6 - Main Notes/eigenvector and eigenvalue\|eigenvectors]] of $A$ with distinct eigenvalues $\lambda_{1},\lambda_{2}$ respectively. Then we have $x_{1}\cdot x_{2}=0$. 

### Proof

Suppose $\langle \mathbf{u}, \mathbf{v} \rangle= \mathbf{u}^T\mathbf{v}.$

$$\begin{align}
\lambda_{1} \langle x_{1},x_{2} \rangle &= \langle \lambda_{1} x_{1}, x_{2}\rangle \\
&= \langle Ax_{1},x_{2}\rangle \\
&= (Ax_{1})^Tx_{2} \\
&= x_{1}^TA^Tx_{2} \\
&= x_{1}^TAx_{2} \\
&= \langle x_{1},Ax_{2}\rangle \\
&= \langle x_{1}, \lambda_{2} x_{2} \rangle \\
&= \lambda_{2} \langle x_{1},x_{2} \rangle.
\end{align}$$
Thus, $(\lambda_{1}-\lambda_{2})\langle x_{1},x_{2} \rangle=0$, but since $\lambda_{1} \neq \lambda_{2}$, we have $\langle x_{1},x_{2} \rangle =0$.