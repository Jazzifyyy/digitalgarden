---
{"dg-publish":true,"permalink":"/6-main-notes/in-a-bivariate-distribution-the-distribution-of-one-variable-conditioned-on-the-other-variable-is-a-normal-distribution/","tags":["probability_theory","info"]}
---

### Statement

Suppose $(X,Y)$ is a [[6 - Main Notes/Bivariate normal distribution\|Bivariate normal distribution]] with means $\mu_{X}, \mu_{Y}$; variances $\sigma_{X}^2, \sigma_{Y}^2$ respectively and correlation $\rho$. Then 
$$X|Y=y \sim \mathcal{N}\!\left( \mu_{X}+ \frac{\rho \sigma_{X}}{\sigma_{Y}}(y-\mu_{Y}),\; \sigma_{X}^2(1-\rho^2) \right)$$
and
$$Y|X=x \sim \mathcal{N}\left(\mu_{Y}+ \frac{\rho \sigma_{Y}}{\sigma_{X}}(x-\mu_{X}), \sigma_{Y}^2(1-\rho) \right).$$
### Proof

$$\begin{align}
f_{X|Y=y}(x|y) &= \frac{f_{X,Y}(x,y)}{f_{Y}(y)} \\[6pt]
&= \frac{\dfrac{1}{2\pi \sigma_{X}\sigma_{Y}\sqrt{ 1-\rho^2 }}
\exp\left\{ -\frac{1}{2(1-\rho^2)}\left[\left(\tfrac{x-\mu_{X}}{\sigma_{X}}\right)^2+ \left(\tfrac{y - \mu_{Y}}{\sigma_{Y}}\right)^2 - 2\rho \left(\tfrac{x-\mu_{X}}{\sigma_{X}}\right)\left(\tfrac{y-\mu_{Y}}{\sigma_{Y}}\right)\right] \right\}}
{\dfrac{1}{\sigma_{Y}\sqrt{ 2\pi }}\exp\left\{ -\tfrac{1}{2}\left(\tfrac{y-\mu_{Y}}{\sigma_{Y}}\right)^2 \right\}} \\[10pt]
&=\frac{1}{\sqrt{ 2\pi(1-\rho^2) }\sigma_{X}}
\exp\left\{ -\frac{1}{2(1-\rho^2)}\left[\rho^2\left(\tfrac{y-\mu_{Y}}{\sigma_{Y}}\right)^2 -2\rho\left(\tfrac{x-\mu_{X}}{\sigma_{X}}\right)\left(\tfrac{y-\mu_{Y}}{\sigma_{Y}}\right)+\left(\tfrac{x-\mu_{X}}{\sigma_{X}}\right)^2\right] \right\} \\[10pt]
&= \frac{1}{\sqrt{ 2\pi (1-\rho^2) }\sigma_{X}}
\exp\left\{ - \frac{1}{2(1-\rho^2)\sigma_{X}^2} \left[x-\left(\mu_{X}+ \rho \sigma_{X}\tfrac{y-\mu_{Y}}{\sigma_{Y}}\right)\right]^2 \right\} \\[10pt]
&\equiv \mathcal{N}\!\left( \mu_{X}+ \frac{\rho \sigma_{X}}{\sigma_{Y}}(y-\mu_{Y}),\; \sigma_{X}^2(1-\rho^2) \right).
\end{align}$$

Similarly,
$$f_{Y|X=x}(y|x) \equiv \mathcal{N}\!\left( \mu_{Y}+ \frac{\rho \sigma_{Y}}{\sigma_{X}}(x-\mu_{X}),\; \sigma_{Y}^2(1-\rho^2) \right).$$