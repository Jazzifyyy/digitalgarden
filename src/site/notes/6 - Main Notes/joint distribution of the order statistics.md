---
{"dg-publish":true,"permalink":"/6-main-notes/joint-distribution-of-the-order-statistics/","tags":["inference","info"]}
---

### Statement

Suppose $X_{1},\dots,X_{n} \sim \mathcal{F}_{\theta}$, where $\mathcal{F}_{\theta}$ is a continuous, and $X_{1},\dots,X_{n}$ are independent. 

The joint distribution of the order statistics are then
$$f_{X_{(1)},\dots,X_{(n)}}(y_{1},\dots,y_{n}) = \begin{cases}
n!\prod_{i=1}^n f_{X_{i}}(x_{i}); \text{ if }y_{1}<\dots<y_{n} \\ \\

0; \text{ otherwise}.
\end{cases}$$

