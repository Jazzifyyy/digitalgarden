---
{"dg-publish":true,"permalink":"/6-main-notes/assignment-1-problem-3-linear-combinations-of-bivariate-normals/","tags":["probability_theory","problem"]}
---

### Problem

Show that if $V$ and $W$ have a bivariate normal distribution then
1. Every linear combination $aV+bW$ has a normal distribution;
2. Every pair of linear combinations $(aV+bW,cV+dW)$ have a bivariate normal distribution;
3. Find the parameters of the distributions in part 1 and part 2 in terms of the parameters of the joint distribution of $V$ and $W$.

### Solution

##### Part 1

Since $V,W$ are two bivariate normal random variables. Then there exists independent standard normal random variables $Z_{1},Z_{2}$ such that
$$V=\sigma_{V}Z_{1}+\mu_{V}$$
and
$$W = \sigma_{W}(\rho Z_{1}+\sqrt{ 1-\rho^2 }Z_{2})+\mu_{W}.$$
Note the following
$$\begin{align}
aV+bW &= a\sigma_{V}Z_{1}+a\mu_{V}+b\sigma_{W}\rho Z_{1}+b\sigma_{W}\sqrt{ 1-\rho^2 }Z_{2}+b\mu_{W} \\
&=(a\sigma_{V}+b\sigma_{W}\rho)Z_{1}+(b\sigma_{W}\sqrt{ 1-\rho^2 })Z_{2}+a\mu_{V}+b\mu_{W} \\
&\sim \mathcal{N}(a\mu_{V}+b \mu_{W}, a^2\sigma_{V}^2+b^2\sigma_{W}^2).
\end{align}$$
##### Part 2

