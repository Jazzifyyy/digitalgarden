---
{"dg-publish":true,"permalink":"/6-main-notes/bivariate-normal-distribution/","tags":["probability_theory","info"]}
---

### Definition

Two random variables $X$ and $Y$ are said to have a **bivariate normal distribution** with parameters $\mu_{X},\sigma_{X}^2,\mu_{Y},\sigma^2_{Y}, \rho$, if their joint pdf is given by
$$f_{X,Y}(x,y)=\frac{1}{2\pi \sigma_{X}\sigma_{Y}\sqrt{ 1-\rho^2 }}\exp\left\{ -\frac{1}{2(1-\rho^2)}\left[\left(\frac{x-\mu_{X}}{\sigma_{X}}\right)^2+ \left(\frac{y - \mu_{Y}}{\sigma_{Y}}\right)^2- 2\rho \left(\frac{y-\mu_{Y}}{\sigma_{Y}}\right)\left(\frac{x-\mu_{X}}{\sigma_{X}}\right)\right] \right\}$$
where $\mu_{X},\mu_{Y} \in \mathbb{R}, \sigma_{X}, \sigma_{Y}>0$ and $\rho \in (-1,1)$.

### Notation

Write this as
$$(X,Y) \sim \mathcal{N}_{2}\left(\begin{pmatrix}
\mu_{X} \\
\mu_{Y}
\end{pmatrix}, \begin{pmatrix}
\sigma_{X}^2 & \rho \sigma_{X}\sigma_{Y} \\
\rho \sigma_{X}\sigma_{Y} & \sigma_{Y}^2
\end{pmatrix}\right).$$
### Construction
+ [[6 - Main Notes/Construction of the bivariate normal distribution\|Construction of the bivariate normal distribution]]