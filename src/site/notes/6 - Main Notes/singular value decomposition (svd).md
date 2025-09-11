---
{"dg-publish":true,"permalink":"/6-main-notes/singular-value-decomposition-svd/","tags":["linear_algebra","info"]}
---

The generalization of the [[6 - Main Notes/spectral decomposition of a matrix\|spectral decomposition of a matrix]] to non-symmetric matrices is known as the **singular value decomposition (SVD)**.
### Statement

A nonzero real $m \times n$ matrix $A$ of rank $r>0$ can be factored as
$$A=P \Sigma Q^T,$$
where $P$ is a $m \times r$ matrix with orthonormal columns, i.e., $P^TP=I$, and $\Sigma$ is a $r \times r$ diagonal matrix with the [[6 - Main Notes/singular values of a matrix\|singular values]] of $A$ as its diagonal entries, and a $r \times n$ matrix $Q^T$ with orthonormal rows, i.e., $Q^TQ=I$.

### Proof

Rewrite the factorization as
$$AQ =P \Sigma$$
where the individual columns of the matrix equation are the vector equations
$$A\mathbf{q}_{i}=\sigma_{i}\mathbf{p}_{i}$$
for all $i \in \{ 1,\dots,r \}$. 

(...)

### Examples
+ [[6 - Main Notes/examples of svd\|examples of svd]]