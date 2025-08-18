---
{"dg-publish":true,"permalink":"/6-main-notes/construction-of-the-bivariate-normal-distribution/","tags":["probability_theory","info"]}
---

### Construction

Suppose $Z_{1},Z_{2} \sim N(0,1)$ and are independent.

For $\mu_{X},\mu_{Y} \in \mathbb{R}, \sigma_{X}, \sigma_{Y}>0$ and $\rho \in (-1,1)$, define 
$$X = \sigma_{X}Z_{1}+ \mu_{X}$$
and
$$Y = \sigma_{Y}(\rho Z_{1}+ \sqrt{ 1- \rho^2 }Z_{2})+ \mu_{Y}.$$

Then the joint pdf of $(X,Y)$ follows a [[6 - Main Notes/Bivariate normal distribution\|bivariate normal distribution]].

### Proof

Define the function $h: \mathbb{R}^2 \rightarrow \mathbb{R}^2$ by 
$$h(z_{1},z_{2})= \left(\sigma_{X}z_{1}+\mu_{X},\sigma_{Y}\left(\rho z_{1}+ \sqrt{ 1- \rho^2 }z_{2}\right)+\mu_{Y} \right).$$
Note that
$$h^{-1}(x,y)=\left(\frac{x-\mu_{X}}{\sigma_{X}}, \frac{1}{\sqrt{ 1-\rho^2 }}\left(\frac{y-\mu_{Y}}{\sigma_{Y}}\right)- \frac{\rho}{\sqrt{ 1-\rho^2 }}\left(\frac{x-\mu_{X}}{\sigma_{X}}\right)\right).$$
Also note that
$$J = \det \begin{pmatrix}
\frac{\partial h_{1}}{\partial z_{1}} & \frac{\partial h_{1}}{\partial z_{2}} \\
\frac{\partial h_{2}}{\partial z_{1}} & \frac{\partial h_{2}}{\partial z_{2}}
\end{pmatrix} = \begin{pmatrix}
\sigma_{X} & 0 \\
\rho \sigma_{Y} & \sigma_{Y}\sqrt{ 1- \rho^2 }
\end{pmatrix} = \sigma_{X}\sigma_{Y}\sqrt{ 1-\rho^2 }.$$

$$\begin{align*}
f_{X,Y}(x,y)&= f_{Z_{1},Z_{2}}(h^{-1}(x,y))\cdot |J|^{-1}\\
&= \left( \frac{1}{\sqrt{ 2\pi }}\exp \left\{ - \frac{1}{2}\left(\frac{x-\mu_{X}}{\sigma_{X}}\right)^2 \right\} \right)\cdot\left( \frac{1}{\sqrt{ 2\pi }}\exp\left\{ -\frac{1}{2(1-\rho^2)}\left[\left(\frac{y - \mu_{Y}}{\sigma_{Y}}\right) - \rho \left(\frac{x-\mu_{X}}{\sigma_{X}}\right) \right]^2 \right\} \right) \cdot |J|^{-1}\\
&= \left( \frac{1}{\sqrt{ 2\pi }}\exp \left\{ - \frac{1}{2}\left(\frac{x-\mu_{X}}{\sigma_{X}}\right)^2 \right\} \right)\cdot\left( \frac{1}{\sqrt{ 2\pi }}\exp\left\{ -\frac{1}{2(1-\rho^2)}\left[\left(\frac{y - \mu_{Y}}{\sigma_{Y}}\right)^2 + \rho^2 \left(\frac{x-\mu_{X}}{\sigma_{X}}\right)^2- 2\rho \left(\frac{y-\mu_{Y}}{\sigma_{Y}}\right)\left(\frac{x-\mu_{X}}{\sigma_{X}}\right) \right] \right\} \right) \cdot |J|^{-1}\\
&= \frac{1}{2\pi}\cdot\exp\left\{ -\frac{1}{2(1-\rho^2)}\left[\left(\frac{y - \mu_{Y}}{\sigma_{Y}}\right)^2 + \rho^2 \left(\frac{x-\mu_{X}}{\sigma_{X}}\right)^2- 2\rho \left(\frac{y-\mu_{Y}}{\sigma_{Y}}\right)\left(\frac{x-\mu_{X}}{\sigma_{X}}\right)+(1-\rho^2) \left(\frac{x-\mu_{X}}{\sigma_{X}}\right)^2 \right] \right\} \cdot |J|^{-1}\\
&= \frac{1}{2\pi \sigma_{X}\sigma_{Y}\sqrt{ 1-\rho^2 }}\cdot\exp\left\{ -\frac{1}{2(1-\rho^2)}\left[\left(\frac{x-\mu_{X}}{\sigma_{X}}\right)^2+ \left(\frac{y - \mu_{Y}}{\sigma_{Y}}\right)^2- 2\rho \left(\frac{y-\mu_{Y}}{\sigma_{Y}}\right)\left(\frac{x-\mu_{X}}{\sigma_{X}}\right)\right] \right\}\\
\end{align*}$$