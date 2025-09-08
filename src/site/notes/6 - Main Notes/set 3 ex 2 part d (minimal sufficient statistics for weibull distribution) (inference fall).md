---
{"dg-publish":true,"permalink":"/6-main-notes/set-3-ex-2-part-d-minimal-sufficient-statistics-for-weibull-distribution-inference-fall/","tags":["inference","problem"]}
---

### Problem

Find the minimal sufficient statistics for the unknown paramaters for a random sample $X_{1},\dots,X_{n}$ from $\text{Weibull}(\lambda,k)$.

The $\text{Weibull}(\lambda,k)$ is a continuous distribution with pdf
$$f_{\lambda,k}(x)=\begin{cases}
\frac{\lambda}{k}\left( \frac{x}{\lambda} \right)^{k-1}e^{- (x/\lambda)^k}; \text{ if }x\geq 0 \\ \\

0; \text{ otherwise}.
\end{cases}$$
### Solution
The ratios of the joint distribution is
$$\frac{p_{\theta}(\mathbf{x})}{p_{\theta}(\mathbf{y})} = \exp \left\{  -\frac{1}{\lambda^k}\left[\sum_{i=1}^nx_{i}^k-\sum_{i=1}^n y_{i}^k\right] \right\}.\left( \frac{\prod_{i=1}^n x_{i}}{\prod_{i=1}^n y_{i}} \right)^{k-1}.$$
The ratio is free of $\theta$ iff $(x_{(1)},\dots,x_{(n)})=(y_{(1)},\dots,y_{(n)})$. Thus $(X_{(1)},\dots,X_{(n)})$ is a minimal statistic for this model. 

