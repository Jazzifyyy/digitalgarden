---
{"dg-publish":true,"permalink":"/6-main-notes/a-real-positive-definite-matrix-can-be-expressed-as-the-product-of-a-non-singular-matrix-and-its-transpose/","tags":["linear_algebra","info"]}
---

### Statement

Suppose $A$ is a real [[6 - Main Notes/positive definite matrix\|positive definite matrix]]. Then there exists a non-singular matrix $B$ such that $A=BB^T$.

### Proof

Since $A$ is symmetric, it is also an [[6 - Main Notes/orthogonally diagonalizable matrix\|orthogonally diagonalizable matrix]] (See: [[6 - Main Notes/a real square matrix is orthogonally diagonalizable iff it is symmetric\|a real square matrix is orthogonally diagonalizable iff it is symmetric]]). 

Thus, 
$$D=S^TAS \implies A=SDS^T=SD^{1/2}(D^{1/2})^TS^T=(SD^{1/2})(SD^{1/2})^T=BB^T.$$
Note that $\det S \neq 0$ and $\det D \neq 0$ since $A$ is positive definite ([[6 - Main Notes/a positive definite matrix is non-singular\|a positive definite matrix is non-singular]]).