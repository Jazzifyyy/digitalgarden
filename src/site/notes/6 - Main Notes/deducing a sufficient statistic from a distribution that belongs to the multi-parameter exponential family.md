---
{"dg-publish":true,"permalink":"/6-main-notes/deducing-a-sufficient-statistic-from-a-distribution-that-belongs-to-the-multi-parameter-exponential-family/","tags":["inference","info"]}
---

### Statement

Suppose $f_{\theta}(\cdot)$, where $\theta=(\theta_{1},\dots,\theta_{k})$, is a pdf/pmf that belongs to the [[6 - Main Notes/multiparameter exponential family\|multiparameter exponential family]], i.e., 
$$f_{\theta}(x)=c(x).\exp \left\{  \sum_{j=1}^k  a_{j}(\theta) \tau_{j}(x)-b(\theta))  \right\}.$$

Then $$T(\mathbf{X})=\left( \sum_{i=1}^n \tau_{1}(X_{i}) ,\dots,\sum_{i=1}^n \tau_{k}(X_{i}) \right)$$ is a [[6 - Main Notes/sufficient statistic\|sufficient statistic]] for $\theta$. 

### Proof

The joint pdf/pmf is given by
$$\begin{align}
p_{\theta}(\mathbf{x}) &= \prod_{i=1}^n \left[ c(x_{i}).\exp \left\{  \sum_{j=1}^ka_{j}(\theta)\tau_{j}(x_{i})-b(\theta)  \right\} \right] \\
&= \exp \left\{  \sum_{i=1}^n \left[ \sum_{j=1}^k a_{j}(\theta)\tau_{j}(x_{i})-b(\theta) \right]  \right\}.\prod_{i=1}^n c(x_{i}) \\
&= \exp \left\{  \sum_{j=1}^k \left[ a_{j}(\theta)\sum_{i=1}^n \tau_{j}(x_{i}) \right] -nb(\theta) \right\}.\prod_{i=1}^n c(x_{i}) \\
&= g_{\theta}(T(\mathbf{x}))h(\mathbf{x})
\end{align}$$
where $g_{\theta}(\mathbf{t})=\exp \left\{  \mathbf{a}(\theta)^T\mathbf{t}-nb(\theta)  \right\}$, $T(\mathbf{x})=\left(\sum_{i=1}^n \tau_{1}(x_{i}), \dots,\sum_{i=1}^n \tau_{k}(x)\right)^T$, $h(\mathbf{x})=\prod_{i=1}^n c(x_{i})$ and $\mathbf{a}(\theta)=(a_{1}(\theta),\dots,a_{k}(\theta))$.

By the [[6 - Main Notes/Fisher-Neyman factorization theorem\|Fisher-Neyman factorization theorem]], we have that $T(\mathbf{X})=\left( \sum_{i=1}^n \tau_{1}(X_{i}) ,\dots,\sum_{i=1}^n \tau_{k}(X_{i}) \right)$ is sufficient for $\theta$.