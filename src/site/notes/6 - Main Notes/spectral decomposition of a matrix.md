---
{"dg-publish":true,"permalink":"/6-main-notes/spectral-decomposition-of-a-matrix/","tags":["linear_algebra","info"]}
---

### Statement

Suppose $A$ is a real symmetric matrix. Then $A$ has the spectral decomposition 
$$A=SDS^T=\lambda_{1}\mathbf{u}_{1}\mathbf{u}_{1}^T+\lambda_{2}\mathbf{u}_{2}\mathbf{u}_{2}^T+\dots + \lambda_{n}\mathbf{u}_{n}\mathbf{u}_{n}^T$$
where $S$ is an orthogonal matrix whose columns are the orthonormal eigenvectors and $D$ is a real diagonal matrix whose diagonal entries are the corresponding eigenvalues. 
### Proof

If $A$ is symmetric, then it is an [[6 - Main Notes/orthogonally diagonalizable matrix\|orthogonally diagonalizable matrix]] (See: [[6 - Main Notes/a real square matrix is orthogonally diagonalizable iff it is symmetric\|a real square matrix is orthogonally diagonalizable iff it is symmetric]]).

Thus, for diagonal matrix $D$ and orthogonal matrix $S$, we have
$$D=S^TAS \implies A=SDS^T.$$
Since $A$ is symmetric, by the [[6 - Main Notes/spectral theorem\|spectral theorem]], there exists eigenvectors $\{\mathbf{v}_{1},\dots,\mathbf{v}_{n}\}$, where $\mathbf{v}_{i}\cdot \mathbf{v}_{j}=0$ for $i \neq j$ and $\mathbf{v}_{i} \cdot \mathbf{v}_{i}=1$ for all $i$, such that
$$\begin{align}
A\mathbf{v}_{i} = \lambda \mathbf{v}_{i} &\implies AS=SD\\
&\implies A=SDS^T
\end{align}$$
where the columns of $S$ are the eigenvectors of $A$, and the diagonals of $D$ are the eigenvalues.