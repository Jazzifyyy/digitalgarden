---
{"dg-publish":true,"permalink":"/6-main-notes/variance-covariance-matrix/","tags":["probability_theory","info"]}
---

### Definition

Suppose we have a random vector $\mathbf{X}=(X_{1},\dots,X_{n})^T$ where the entries of the vectors are random variables with finite expectation and variance. 

Then each entry of the **variance-covariance matrix** $\Sigma$ of $\mathbf{X}$ is given by
$$\Sigma_{(i,j)}= \text{cov}[X_{i},X_{j}]= \mathbb{E}[(X_{i}- \mathbb{E}[X_{i}])(X_{j} - \mathbb{E}[X_{j}])].$$
### Expanded form for $n=2$

We have
$$\Sigma_{2 \times 2}= \begin{bmatrix}
\text{Var}(X) & \text{Cov}(X,Y)  \\
\text{Cov}(Y,X) & \text{Var}(Y)
\end{bmatrix}.$$

### Also See:
+ [[6 - Main Notes/The variance-covariance matrix is positive-semidefinite (non-negative definite)\|The variance-covariance matrix is positive-semidefinite (non-negative definite)]]