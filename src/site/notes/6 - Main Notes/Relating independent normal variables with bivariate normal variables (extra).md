---
{"dg-publish":true,"permalink":"/6-main-notes/relating-independent-normal-variables-with-bivariate-normal-variables-extra/","tags":["probability_theory","info"]}
---

### Statement

Suppose $X$ and $Y$ are two [[6 - Main Notes/Standard bivariate normal distribution\|bivariate normal distributions]]. Then there exist standard normal random variables $Z_{1}$ and $Z_{2}$ such that $X$and $Y$ can be expressed as:
$$\begin{align}
X &= \sigma_{X}Z_{1} + \mu_{X} \\ \\
Y&= \sigma_{Y}(\rho Z_{1} + \sqrt{ 1- \rho^2 }Z_{2}) + \mu_{Y}.
\end{align}$$
### Proof

Set
$$Z_{1}= \frac{X-\mu}{\sigma_{X}}$$
and
$$Z_{2}= - \frac{\rho}{\sqrt{ 1- \rho^2 }} \frac{X-\mu_{X}}{\sigma_{X}} + \frac{1}{\sqrt{ 1- \rho^2 }} \frac{Y-\mu_{Y}}{\sigma_{Y}}.$$

