---
{"dg-publish":true,"permalink":"/6-main-notes/construction-of-the-standard-bivariate-normal-distribution/","tags":["info","probability_theory"]}
---

### Construction

Suppose $Z_{1},Z_{2}$ are two independent $N(0,1)$ random variables. Define
$$\begin{align}
X &= Z_{1}, \\
Y &= \rho Z_{1}+ \sqrt{ 1- \rho^2 }Z_{2},
\end{align}$$
where $\rho \in (-1,1)$. 

Then the joint pdf of $(X,Y)$ follows a [[6 - Main Notes/Standard bivariate normal distribution\|a standard bivariate normal distribution]].

### Proof

Define the function $h: \mathbb{R}^2 \rightarrow \mathbb{R}^2$ by 
$$h(z_{1},z_{2})= \left(z_{1},\rho z_{1}+ \sqrt{ 1- \rho^2 }z_{2} \right).$$
Note that $h^{-1}(x,y)=\left( x, \frac{y}{\sqrt{ 1- \rho^2 }}- \frac{\rho }{\sqrt{ 1-\rho^2 }}x \right)$.

Also note that 
$$J = \det \begin{pmatrix}
\frac{\partial h_{1}}{\partial z_{1}} & \frac{\partial h_{1}}{\partial z_{2}} \\
\frac{\partial h_{2}}{\partial z_{1}} & \frac{\partial h_{2}}{\partial z_{2}}
\end{pmatrix} = \det\begin{pmatrix}
1 & 0 \\
\rho & \sqrt{ 1- \rho^2 }
\end{pmatrix} = \sqrt{ 1- \rho^2 }.$$


The joint pdf of $(X,Y)$ is given by
$$\begin{align*}
f_{X,Y}(x,y)&= f_{Z_{1},Z_{2}}(h^{-1}(x,y))\cdot |J|^{-1}\\
&= \left( \frac{1}{\sqrt{ 2\pi }}\exp\left\{ -\frac{x^2}{2} \right\} \right)\cdot\left( \frac{1}{\sqrt{ 2\pi }}\exp\left\{ -\frac{(y - \rho x)^2}{2(1-\rho^2)} \right\} \right) \cdot |J|^{-1} \\
&= \frac{1}{2\pi}\exp\left\{  -\frac{1}{2} \left[ x^2 + \frac{(y- \rho x)^2}{1- \rho^2} \right] \right\} \cdot \frac{1}{\sqrt{ 1- \rho^2 }} \\
&= \frac{1}{2\pi \sqrt{ 1- \rho^2 }} \exp \left\{  -\frac{x^2 - \rho^2 x^2 + y^2 + \rho^2x^2 - 2\rho xy}{2(1- \rho^2)}  \right\} \\
&= \frac{1}{2\pi \sqrt{ 1- \rho^2 }}\exp \left\{ - \frac{x^2 -2 \rho xy + y^2}{2(1- \rho^2)} \right\}.
\end{align*}$$
### Additional Insights
1. $X$ and $Y$ are not necessarily independent.
2. If $\rho=0$, then $X$ and $Y$ are independent. 
3. The distribution of $Y$ is $N(0,1)$:
$$\begin{align*}
   f_{Y}(y) &= \int_{-\infty}^\infty f_{X,Y}(x,y)dy \\
   &= \frac{1}{2\pi \sqrt{ 1-\rho^2 }}\int_{-\infty}^\infty \exp \left\{ - \frac{x^2 -2 \rho xy + y^2}{2(1- \rho^2)} \right\}dx \\
   &= \frac{1}{2\pi \sqrt{ 1-\rho^2 }}\int_{-\infty}^\infty \exp \left\{ - \frac{(x - \rho y)^2 + y^2(1- \rho^2)}{2(1- \rho^2)} \right\}dx \\
   &= \frac{1}{2\pi \sqrt{ 1-\rho^2 }}\int_{-\infty}^\infty \exp \left\{ - \frac{(x - \rho y)^2}{2(1- \rho^2)} - \frac{y^2}{2}\right\} dx\\
   &\text{Setting } t = \frac{x- \rho y}{\sqrt{ 1 - \rho^2 }} \text{ with } dx = dt \sqrt{ 1 - \rho^2 } \text{ yields: }\\
   &= \frac{e^{-y^2/2}}{2\pi}\int_{-\infty}^\infty e^{-t^2/2} dt \\
   &= \frac{1}{\sqrt{ 2\pi }}e^{-y^2/2}.
   \end{align*}$$

### Also See:
+ If we want two jointly normal random variables $X$ and $Y$ such that $X \sim N(\mu_{X},\sigma_{X}^{2})$ and $Y \sim N(\mu_{Y}, \sigma^2_{Y})$, then see: [[6 - Main Notes/Construction of the bivariate normal distribution\|Construction of the bivariate normal distribution]].