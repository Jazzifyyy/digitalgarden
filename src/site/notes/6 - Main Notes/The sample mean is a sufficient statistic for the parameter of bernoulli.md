---
{"dg-publish":true,"permalink":"/6-main-notes/the-sample-mean-is-a-sufficient-statistic-for-the-parameter-of-bernoulli/","tags":["inference","info"]}
---

### Statement

Suppose $X_{1},\dots,X_{n} \sim Bern(p)$ and are independent. Then $T(\mathbf{X})= \sum_{i=1}^n X_{i}$ is a [[6 - Main Notes/sufficient statistic\|sufficient statistic]] for $p$.

### Proof

The joint distribution of $X_{1},\dots,X_{n}$ is given by
$$\begin{align}
p_{\theta}(\mathbf{x}) &= \prod_{i=1}^n f_{\theta}(x_{i}) \\
&= \prod_{i=1}^n \{ p^{x_{i}}(1-p)^{x_{i}} \} \\
&= p^{\sum_{i=1}^n x_{i}}(1-p)^{n-\sum_{i=1}^nx_{i}}.
\end{align}$$
Note that $T(\mathbf{X})= \sum_{i=1}^n X_{i} \sim \text{Binom}(n,p)$.

The conditional distribution of $\mathbf{X}$ given $T(\mathbf{X})=t$ where $t \in \{ 0,\dots,n \}$ is given by
$$\mathbb{P}_{\theta} \{ \mathbf{X}=\mathbf{x} | T(\mathbf{X})=t \} = \frac{\mathbb{P}_{\theta}(\{ \mathbf{X} = \mathbf{x} \} \cap \{ T(\mathbf{X})=t \})}{\mathbb{P}_{\theta}\{ T(\mathbf{X})=t \}}.$$
##### Case 1

If $T(\mathbf{x}) \neq t$, then we have $\mathbb{P}_{\theta} \{ \mathbf{X}=\mathbf{x} | T(\mathbf{X})=t \}=0$ since the numerator in the above expression is zero.

##### Case 2

If $T(\mathbf{x})=t$, then we have 
$$\begin{align}
\frac{\mathbb{P}_{\theta}(\{ \mathbf{X} = \mathbf{x} \} \cap \{ T(\mathbf{X})=t \})}{\mathbb{P}_{\theta}\{ T(\mathbf{X})=t \}}
&= \frac{p_{\theta}(\mathbf{x})}{\mathbb{P}_{\theta}(T(\mathbf{X})=t)}  \\
&= \frac{p^{\sum_{i=1}^nx_{i}}(1-p)^{n - \sum_{i=1}^n x_{i}}}{{n \choose t}p^t(1-p)^{n-t}} \\
&= \frac{1}{{n \choose t}}.
\end{align}$$

##### The distribution

Thus,
$$\mathbb{P}_{\theta} \{ \mathbf{X} = \mathbf{x} | T(\mathbf{X})=t \} = \begin{cases}
0; \text{ if }T(\mathbf{x}) \neq t \\
\frac{1}{{n \choose t}}; \text{ if }T(\mathbf{x})=t
\end{cases}$$
which is a distribution free of $\theta$.