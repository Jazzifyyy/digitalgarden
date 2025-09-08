---
{"dg-publish":true,"permalink":"/6-main-notes/deducing-a-sufficient-statistic-from-a-distribution-that-belongs-to-the-one-parameter-exponential-family/","tags":["inference","info"]}
---

### Statement

Suppose $f_{\theta}(\cdot)$ is a pdf/pmf that belongs to the [[6 - Main Notes/one-parameter exponential family\|one-parameter exponential family]], i.e., $f_{\theta}(x)=c(x).\exp \{ a(\theta) \tau(x)-b(\theta)) \}$.

Then $T(\mathbf{X})=\sum_{i=1}^n \tau(X_{i})$ is a [[6 - Main Notes/sufficient statistic\|sufficient statistic]] for $\theta$. 

### Proof

The joint pmf/pdf is given by
$$\begin{align}
p_{\theta}(\mathbf{x}) &= \prod_{i=1}^n f_{\theta}(x_{i}) \\
&= \prod_{i=1}^n c(x_{i})\exp \{ a(\theta)\tau(x_{i})-b(\theta) \} \\
&= \exp \left\{  a(\theta)\sum_{i=1}^n \tau(x_{i})-nb(\theta)  \right\}.\prod_{i=1}^n c(x_{i}) \\
&= g_{\theta}(T(\mathbf{x}))h(\mathbf{x})
\end{align}$$
where $g_{\theta}(t)=\exp \{ a(\theta)t-nb(\theta) \}$, $T(\mathbf{x})=\sum_{i=1}^n \tau(x_{i})$, $h(\mathbf{x})=\prod_{i=1}^n c(x_{i})$.

By the [[6 - Main Notes/Fisher-Neyman factorization theorem\|Fisher-Neyman factorization theorem]], we have that $T(\mathbf{X})=\sum_{i=1}^n \tau(X_{i})$ is sufficient for $\theta$.