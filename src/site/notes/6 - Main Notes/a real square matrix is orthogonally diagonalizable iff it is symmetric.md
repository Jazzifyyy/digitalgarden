---
{"dg-publish":true,"permalink":"/6-main-notes/a-real-square-matrix-is-orthogonally-diagonalizable-iff-it-is-symmetric/","tags":["linear_algebra","info"]}
---

### Statement

A real square matrix is an [[6 - Main Notes/orthogonally diagonalizable matrix\|orthogonally diagonalizable matrix]] iff it is symmetric.

### Proof

Suppose $A$ is orthogonally diagonalisable, then there exists a diagonal matrix $D$ and an orthogonal matix $S$ such that $D=S^TAS$, which implies that $A^T=(SDS^T)^T=SDS^T=A$ and therefore, $A$ is symmetric.

[[6 - Main Notes/the dot product of two eigenvectors (with distinct eigenvalues) of a symmetric matrix is zero\|the dot product of two eigenvectors (with distinct eigenvalues) of a symmetric matrix is zero]]

### Corollary
+ [[6 - Main Notes/a real positive definite matrix can be expressed as the product of a non-singular matrix and its transpose\|a real positive definite matrix can be expressed as the product of a non-singular matrix and its transpose]]