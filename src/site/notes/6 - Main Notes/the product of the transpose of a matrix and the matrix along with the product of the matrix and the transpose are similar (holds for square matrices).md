---
{"dg-publish":true,"permalink":"/6-main-notes/the-product-of-the-transpose-of-a-matrix-and-the-matrix-along-with-the-product-of-the-matrix-and-the-transpose-are-similar-holds-for-square-matrices/","tags":["linear_algebra","info"]}
---

### Statement

Suppose $A$ is a $n \times n$ matrix. Then $AA^T$ and $AA^T$ are [[6 - Main Notes/similar matrices\|similar matrices]].

### Proof

By the [[6 - Main Notes/polar decomposition\|polar decomposition]], we have
$$AA^T=(GV)(GV)^T=GVV^TG^T=GG^T$$
and
$$A^TA=(GV)^T(GV)=V^TG^TGV=V^T(AA^T)V.$$
Note that since $V$ is orthogonal, we have $V^T=V^{-1}$ and we are done. 