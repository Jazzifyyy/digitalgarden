---
{"dg-publish":true,"permalink":"/6-main-notes/a-square-matrix-has-full-rank-iff-it-is-invertible/","tags":["linear_algebra","info"]}
---

### Statement

Suppose $A \in \mathbb{M}_{n}(\mathbb{R})$. Then $A$ is invertible iff it has full rank.

### Proof

Suppose $A$ is invertible, i.e., there exists $A^{-1}$ such that $AA^{-1}=I$. Note that $\{ Av \mid v \text{ is a column of }A^{-1} \}=\{ e_{1},\dots,e_{n} \}$ where $e_{i}$'s are the standard of $\mathbb{R}^n$. Thus, any vector $x \in \mathbb{R}^n$ can be expressed as
$$\begin{align}
x&=x_{1}e_{1}+\dots+x_{n}e_{n} \\
&=x_{1}[(a_{1}v_{1,1})+\dots +(a_{n}v_{n,1})]+\dots+x_{n}[(a_{1}v_{1,n})+\dots+(a_{n}v_{n,n})] \\
&= a_{1}(x_{1}v_{1,1}+\dots+x_{n}v_{n,1})+\dots + a_{n}(x_{1}v_{n,1}+\dots+x_{n}v_{n,n}).
\end{align}$$
where $a_{i}$ is the $i$th column of $A$ and $v_{i,j}$ is the $i,j$ th element of $A^{-1}$. 

Therefore, $\text{span}(a_{1},\dots,a_{n})=\mathbb{R}^n$. Also note that
$$Ay=0 \implies y =0$$
and thus the columns forms a basis for $\mathbb{R}^n$ and thus, $\dim C(A)=n$.