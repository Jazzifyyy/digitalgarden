---
{"dg-publish":true,"permalink":"/6-main-notes/linear-regression-model/","tags":["regression","info"]}
---

### Model

Suppose we have the data $(x_{1},y_{1}),\dots,(x_{n},y_{n})$. We use the model 
$$y_{i}= \beta_{0}+\beta_{1}x_{i}+ \varepsilon_{i}$$
where $i \in \{ 1,\dots,n \}$.

### Assumptions

We assume
1. The linear model holds.
2. All $\varepsilon_{1},\dots,\varepsilon_{n}$ are independent.
3. All $\varepsilon_{i}$ are independent of $x_{j}$.
4. We have $\mathbb{E}[\varepsilon_{i}]=0$ and $\text{Var}(\varepsilon_{i})=\sigma^2$ for all $i$.

### Note

1. Often we assume that $x_{i}$ are fixed. Otherwise, we condition on $x_{i}$. 
2. Note that the "randomness" of $\varepsilon_{i}$ implies the same for $y_{i}$.
