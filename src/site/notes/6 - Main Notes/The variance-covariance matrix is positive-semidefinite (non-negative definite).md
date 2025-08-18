---
{"dg-publish":true,"permalink":"/6-main-notes/the-variance-covariance-matrix-is-positive-semidefinite-non-negative-definite/","tags":["probability_theory","info"]}
---

### Statement

The [[6 - Main Notes/variance-covariance matrix\|variance-covariance matrix]] is **positive semi-definite**, i.e., we have
$$x^T \Sigma x \geq 0$$
for all $x \in \mathbb{R}^n$.

### Proof (for $n=2$)

Take any $x \in \mathbb{R}^2$.

Note that
$$\begin{align}
x^T \Sigma x &= (x_{1},x_{2}) \begin{pmatrix}
\text{Var}(X) & \text{Cov}(X,Y)  \\
\text{Cov}(Y,X) & \text{Var}(Y)
\end{pmatrix} \begin{pmatrix}
x_{1} \\
x_{2}
\end{pmatrix} \\ 
&= x_{1}^2 \text{Var}(X) + 2x_{1}x_{2} \text{Cov}(X,Y)+x_{2}^2 \text{Var}(Y) \\
&= \text{Var}(x_{1}X) + \text{Var}(x_{2}Y)+ 2\text{Cov}(x_{1}X,x_{2}Y) \\
&= \text{Var}(x_{1}X+x_{2}Y) \geq 0.
\end{align}$$
(Notice that a quadratic form can be expressed in the form of variance!!)