---
{"dg-publish":true,"permalink":"/6-main-notes/the-order-statistics-are-sufficient/","tags":["inference","info"]}
---

### Statement

Suppose $X_{1},\dots,X_{n} \sim \mathcal{F}_{\theta}$ and are independent ($\mathcal{F}$ is a pdf). Then the order statistics $(X_{(1)},\dots,X_{(n)})$ is [[6 - Main Notes/sufficient statistic\|sufficient]] for $\theta$.

### Proof

Note that the order statistics are distinct with probability $1$: $$X_{(1)}<X_{(2)}<\dots< X_{(n)}.$$
Recall the [[6 - Main Notes/joint distribution of the order statistics\|joint distribution of the order statistics]].

For some $\mathbf{T}=(t_{1},\dots,t_{n})$, where $t_{1}<\dots<t_{n}$, we have
$$f_{\mathbf{X}|\mathbf{T}}(\mathbf{x}|\mathbf{t})= \frac{f_{\mathbf{X}}(\mathbf{x})}{f_{\mathbf{T}}(\mathbf{t})}= \begin{cases}
\frac{\prod_{i=1}^nf_{X}(x_{i})}{n!\prod_{i=1}^n f_{X}(t_{i})}= \frac{1}{n!}; \text{ if }T(\mathbf{x})=\mathbf{t}; \\ \\

0; \text{ otherwise}
\end{cases}$$