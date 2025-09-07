---
{"dg-publish":true,"permalink":"/6-main-notes/set-3-ex-2-part-a-minimal-sufficient-statistics-for-beta-distribution-inference-fall/","tags":["inference","problem"]}
---

### Problem

Find the minimal sufficient statistics for the unknown paramaters for a random sample $X_{1},\dots,X_{n}$ from $\text{Beta}(\alpha,\beta)$.

### Solution

The joint distribution is given by
$$\begin{align}
p_{\mathbf{X}}(\mathbf{x}) &= \left(\frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)}\right)^n\prod_{i=1}^n[(x_{i}^{a-1})(1-x_{i})^{b-1}\mathbb{1}_{\{ x_{i} \in (0,1) \}}] \\
&= \left( \frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)} \right)^n \left( \prod_{i=1}^n x_{i} \right)^{\alpha-1} \left( \prod_{i=1}^n (1-x_{i})\right)^{b-1} \mathbb{1}_{\{ 0<x_{(1)}<x _{(n)}<1 \}}.
\end{align}$$
Notice that $\frac{p_{\mathbf{X}}(\mathbf{x})}{p_{\mathbf{Y}}(\mathbf{y})}$ is free of $(\alpha,\beta)$ iff $\prod x_{i}= \prod y_{i}$ and $\prod (1-x_{i})=\prod(1-y_{i})$.

Thus, $\left( \prod_{i=1}^n X_{i}, \prod_{i=1}^n (1-X_{i}) \right)$ is minimal sufficient for $(\alpha,\beta)$.