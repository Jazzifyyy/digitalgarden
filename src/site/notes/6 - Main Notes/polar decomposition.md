---
{"dg-publish":true,"permalink":"/6-main-notes/polar-decomposition/","tags":["linear_algebra","info"]}
---

### Statement

A real $n \times n$ matrix $A$ admits the factorization
$$A=GV$$
where $G$ is symmetric and positive semidefinite, and $V$ is orthogonal.

### Proof

By [[6 - Main Notes/singular value decomposition (svd)\|singular value decomposition (svd)]], we have
$$A=P \Sigma Q^T=P\Sigma P^TPQ^T$$
where $P$ is orthogonal and $\Sigma$ is diagonal.

Set $G= P\Sigma P^T$ and $V=PQ^T$.

Note that $G$ is symmetric:
$$G^T=(P\Sigma P^T)^T=(P^T)^T\Sigma^TP^T=P \Sigma P^T=G$$
and semidefinite, i.e., for any $\mathbf{x}$,
$$\mathbf{x}^TG\mathbf{x}=(\mathbf{x}^TP)\Sigma (P^T\mathbf{x})=\sum_{i=1}^n \sigma_{i}(P^Tx)_{i}^2 \geq 0$$
since each $\sigma_{i}\geq 0$.

We also have that $V$ is orthogonal:
$$V^TV=(PQ^T)^T(PQ^T)=QP^TPQ^T=I.$$
