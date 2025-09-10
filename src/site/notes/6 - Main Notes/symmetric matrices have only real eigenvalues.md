---
{"dg-publish":true,"permalink":"/6-main-notes/symmetric-matrices-have-only-real-eigenvalues/","tags":["linear_algebra","info"]}
---

### Statement

Symmetric matrices (the [[6 - Main Notes/conjugate transpose of a matrix\|conjugate transpose]] is equal to itself for complex matrices) have only real [[6 - Main Notes/eigenvector and eigenvalue\|eigenvalues]].

### Proof

Suppose that $A$ is a symmetric matrix and $\lambda$ is the associated eigenvalue for the eigenvector $\mathbf{v}$.

We extend the dot product to complex vectors: $\langle \mathbf{v}, \mathbf{w} \rangle=\mathbf{v}\cdot\mathbf{w}=\sum_{i}\bar{v}_{i}w_{i}$. 

Note that this dot product has the property 
$$\begin{align}
\langle \mathbf{v}, A\mathbf{w} \rangle&=\sum_{i}\bar{v}_{i}\left(\sum_{j} a_{i,j}w_{j}\right) \\
&=\bar{v}_{1}(a_{11}w_{1}+\dots+a_{1n}w_{n})+\bar{v}_{2}(a_{21}w_{1}+\dots+a_{2n}w_{n})+\dots \\
&= (\bar{v}_{1}a_{11}+\dots+\bar{v}_{n}a_{n1})w_{1}+(\bar{v}_{1}a_{12}+\dots+\bar{v}_{n}a_{n2})w_{2}+\dots \\
&= \overline{(v_{1}\bar{a}_{11}+\dots+v_{n}\bar{a}_{n1})}w_{1}+\overline{(v_{1}\bar{a}_{12}+\dots+v_{n}\bar{a}_{n2})}w_{2}+\dots  \\
&= \langle (\bar{A})^T\mathbf{v}, \mathbf{w} \rangle
\end{align}$$
and $\langle \lambda \mathbf{v}, \mathbf{w} \rangle = \bar{\lambda} \langle \mathbf{v}, \mathbf{w} \rangle$ as well as $\langle \mathbf{v}, \lambda \mathbf{w} \rangle=\lambda \langle \mathbf{v}, \mathbf{w} \rangle$.

Now note that
$$\begin{align}
\bar{\lambda}\langle \mathbf{v},\mathbf{v} \rangle &= \langle \mathbf{v}, \lambda \mathbf{v} \rangle \\
&= \langle \mathbf{v}, A\mathbf{v} \rangle \\
&= \langle (\bar{A})^T \mathbf{v}, \mathbf{v}\rangle \\
&= \langle A\mathbf{v},\mathbf{v} \rangle \\
&= \langle \lambda \mathbf{v}, \mathbf{v}\rangle \\
&= \lambda \langle\mathbf{v}, \mathbf{v}\rangle.
\end{align}$$
This shows that $\lambda=\bar{\lambda}$, since $\langle \mathbf{v}, \mathbf{v} \rangle=|v_{1}|^2+\dots+|v_{n}|^2>0$ for non zero $\mathbf{v}$.