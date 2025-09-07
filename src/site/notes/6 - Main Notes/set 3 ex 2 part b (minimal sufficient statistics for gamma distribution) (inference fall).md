---
{"dg-publish":true,"permalink":"/6-main-notes/set-3-ex-2-part-b-minimal-sufficient-statistics-for-gamma-distribution-inference-fall/","tags":["inference","problem"]}
---

### Problem 

Find the minimal sufficient statistics for the unknown paramaters for a random sample $X_{1},\dots,X_{n}$ from $\Gamma(\alpha,\lambda)$.

### Solution

The joint distribution is given by
$$\begin{align}
p_{\mathbf{X}}(\mathbf{x}) &= \left( \frac{\lambda^\alpha}{\Gamma(\alpha)} \right)^n \prod_{i=1}^n[x_{i}^{\alpha-1}e^{-\lambda x_{i}}\mathbb{1}_{\{ x_{i}>0 \}}] \\
&= \left(\frac{\lambda^\alpha}{\Gamma(\alpha)}\right)^n \left(\prod_{i=1}^n x_{i}\right)^{\alpha-1}\exp \left\{  -\lambda \sum_{i=1}^n x_{i}  \right\}\mathbb{1}_{\{ X_{(1)}>0 \}}.
\end{align}$$
Notice that $\frac{p_{\mathbf{X}}(\mathbf{x})}{p_{\mathbf{Y}}(\mathbf{y})}$ is free of $(\alpha,\lambda)$ iff $\prod x_{i}= \prod y_{i}$ and $\sum x_{i}=\sum y_{i}$. 

Thus $\left( \prod_{i=1}^n X_{i}, \sum_{i=1}^n X_{i} \right)$ is minimal sufficient for $(\alpha,\lambda)$. 

We also have $\left( \left( \prod_{i=1}^n X_{i}\right)^{1/n}, \frac{\sum_{i=1}^nX_{i}}{n} \right)$ is minimal sufficient for $(\alpha, \lambda)$, i.e., the AM and the GM are jointly sufficient for the unknown parameters.  