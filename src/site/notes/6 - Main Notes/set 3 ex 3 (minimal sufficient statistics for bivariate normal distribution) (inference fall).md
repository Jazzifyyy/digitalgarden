---
{"dg-publish":true,"permalink":"/6-main-notes/set-3-ex-3-minimal-sufficient-statistics-for-bivariate-normal-distribution-inference-fall/","tags":["inference","problem"]}
---

### Problem

Suppose $(X_{1},Y_{1}),\dots,(X_{n},Y_{n}) \sim \mathcal{N}_{2}(\mu,\Sigma)$ and are independent. Find the minimal sufficient statistics for the parameter $\theta=(\mu_{X}, \mu_{Y}, \sigma_{X}^2,\sigma_{Y}^2,\rho)$ under the following setups:

1. All the parameters are unknown.
2. $\sigma_{X}=\sigma_{Y}=1.$
### Solution

The joint pdf is given by
$$\begin{aligned}
p_{\theta}(\mathbf{x},\mathbf{y}) &= \prod_{i=1}^n\left[\frac{1}{2\pi \sigma _{X}\sigma_{Y}\sqrt{ 1-\rho^2 }}\exp \left\{  -\frac{1}{2(1-\rho^2)}\left[\left( \frac{x_{i}-\mu_{X}}{\sigma_{X}}\right)^2 + \left(\frac{y_{i}-\mu_{Y}}{\sigma_{Y}}\right)-2\rho\left(\frac{x_{i}-\mu_{X}}{\sigma_{X}}\right)\left(\frac{y_{i}-\mu_{Y}}{\sigma_{Y}}\right)\right]\  \right\}\right] \\
&= \left( \frac{1}{2\pi \sigma_{X}\sigma_{Y}\sqrt{ 1-\rho^2 }} \right)^2\exp \left\{  -\frac{1}{2(1-\rho
{ #2}
)}\left[\sum_{i=1}^n \frac{x_{i}^2}{\sigma_{X}^2}+\sum_{i=1}^n \frac{y_{i}^2}{\sigma_{Y}^2}-2\mu_{X}\sum_{i=1}^n \frac{x_{i}}{\sigma_{X}^2}-2\mu_{Y}\sum_{i=1}^n \frac{y_{i}}{\sigma_{Y}^2}-2\rho \sum_{i=1}^n \frac{x_{i}y_{i}}{\sigma_{X}\sigma_{Y}}+\frac{2\rho}{\sigma_{X}\sigma_{Y}}\left( \mu_{X}\sum_{i=1}^n y_{i}+ \mu_{Y}\sum_{i=1}^n x_{i} \right)  -\frac{2n\rho \mu_{X}\mu_{Y}}{\sigma_{X}\sigma_{Y}}\right]  \right\}. 
\end{aligned}$$
Thus
$$\frac{p_{\theta}(\mathbf{x},\mathbf{y})}{p_\theta(\mathbf{x}',\mathbf{y}')}= \exp \left\{  -\frac{1}{2(1-\rho^2)}\left[ \frac{1}{\sigma_{X}^2}\sum_{i=1}^n (x_{i}^2-x_{i}^{'2})+\frac{1}{\sigma_{Y}^2}\sum_{i=1}^n (y_{i}^2-y_{i}^{'2})-\frac{2\mu_{X}}{\sigma_{X}^2}\sum_{i=1}^n(x_{i}-x_{i}')-\frac{2\mu_{Y}}{\sigma_{Y}^2}\sum_{i=1}^n(y_{i}-y_{i}')-\frac{2\rho}{\sigma_{X}\sigma_{Y}} \sum_{i=1}^n(x_{i}y_{i}-x_{i}'y_{i}') \right]  \right\}.$$
##### Part 1

The ratio is free of $\theta$ iff $\sum_{i=1}^n x_{i}^2 = \sum_{i=1}^n x_{i}^{'2}$, $\sum_{i=1}^n y_{i}^2 = \sum_{i=1}^n y_{i}^{'2}$, $\sum_{i=1}^n x_{i} = \sum_{i=1}^n x_{i}'$, $\sum_{i=1}^n y_{i} = \sum_{i=1}^n y_{i}$, $\sum_{i=1}^n x_{i}y_{i} = \sum_{i=1}^n x_{i}'y_{i}'$.

Thus, 
$$\left( \sum_{i=1}^n X_{i}^2, \sum_{i=1}^n Y_{i}^2,\sum_{i=1}^n X_{i}, \sum_{i=1}^n Y_{i}, \sum_{i=1}^n X_{i}Y_{i} \right)$$
is minimal sufficient for $\theta$.

##### Part 2

We have 
$$\left( \sum_{i=1}^n X_{i}^2, \sum_{i=1}^n Y_{i}^2,\sum_{i=1}^n X_{i}, \sum_{i=1}^n Y_{i}, \sum_{i=1}^n X_{i}Y_{i} \right)$$
is minimal sufficient for $(\mu_{X},\mu_{Y},\rho)$.