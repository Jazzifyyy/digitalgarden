---
{"dg-publish":true,"permalink":"/6-main-notes/assignment-3-problem-2/","tags":["probability_theory","problem"]}
---

### Problem

Suppose $X_{1},\dots,X_{n}$ are iid standard normal variables. Let $\mathbf{X}$ be a random vector, i.e., 
$$\mathbf{X}:= \begin{pmatrix}
X_{1} \\
\vdots \\
X_{d}
\end{pmatrix}$$
and let $B$ be a $k \times d$ *rectangular* matrix with real entries and is *full row rank* (i.e., the rows are linearly independent).

Define $\mathbf{W}:= B\mathbf{X}$. Show that $\mathbf{W}$ is a multivariate normal random vector with *mean vector* $\mathbf{0}$
and *variance-covariance matrix* $BB^T$.

### Solution

By the basis extension theorem, we can suitably select some vectors $c_{i}=(c_{i1},\dots,c_{id})$ such that $\{ b_{1},\dots,b_{k},c_{1},\dots,c_{d-k} \}$ is a basis of $\mathbb{R}^d$.

Construct the matrix
$$A:=\begin{pmatrix}
B \\
C
\end{pmatrix}$$
where 
$$C=\begin{pmatrix}
c_{11} & c_{12} & \dots & c_{1d} \\
\vdots & & & \vdots \\
c_{d-k,1} & c_{d-k,2} & & c_{d-k,d}
\end{pmatrix}.$$
Note that $A$ is a square matrix and has dimension $d$ (i.e., full rank). Therefore, $A$ is non-singular.

By [[6 - Main Notes/assignment 3 problem 1\|assignment 3 problem 1]], we have
$$\mathbf{Y}=\begin{pmatrix}
\mathbf{W} \\
\mathbf{Z}
\end{pmatrix}=
\begin{pmatrix}
B \\
C
\end{pmatrix}\mathbf{X}
=A\mathbf{X}\sim \mathcal{N}_{d}(\mathbf{0}, AA^T)$$
where $$AA^T= \begin{pmatrix} B \\
C \end{pmatrix}\Sigma \begin{pmatrix}
B^T | C^T
\end{pmatrix} = \begin{pmatrix}
B \Sigma B^T & B \Sigma C^T \\
C \Sigma B^T & C \Sigma C^T
\end{pmatrix}.$$

Thus, the first $k$ components of $\mathbf{Y}$ are distributed as $\mathbf{W} \sim \mathcal{N}_{k}(\mathbf{0}_{k},BB^T)$.
