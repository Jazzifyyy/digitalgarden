---
{"dg-publish":true,"permalink":"/6-main-notes/bivariate-normal-distribution/","tags":["probability_theory","info"]}
---

### Definition

Two random variables $X$ and $Y$ are said to have a **bivariate normal distribution** with parameters $\mu_{X},\sigma_{X}^2,\mu_{Y},\sigma^2_{Y}, \rho$, if their joint pdf is given by
$$f_{X,Y}(x,y)=\frac{1}{2\pi \sigma_{X}\sigma_{Y}\sqrt{ 1-\rho^2 }}\exp\left\{ -\frac{1}{2(1-\rho^2)}\left[\left(\frac{x-\mu_{X}}{\sigma_{X}}\right)^2+ \left(\frac{y - \mu_{Y}}{\sigma_{Y}}\right)^2- 2\rho \left(\frac{y-\mu_{Y}}{\sigma_{Y}}\right)\left(\frac{x-\mu_{X}}{\sigma_{X}}\right)\right] \right\}$$
where $\mu_{X},\mu_{Y} \in \mathbb{R}, \sigma_{X}, \sigma_{Y}>0$ and $\rho \in (-1,1)$.
##### Notation

Write this as
$$(X,Y) \sim \mathcal{N}_{2}\left(\begin{pmatrix}
\mu_{X} \\
\mu_{Y}
\end{pmatrix}, \begin{pmatrix}
\sigma_{X}^2 & \rho \sigma_{X}\sigma_{Y} \\
\rho \sigma_{X}\sigma_{Y} & \sigma_{Y}^2
\end{pmatrix}\right).$$
### Alternate Expression

Consider the random vector $\mathbf{Z}=(X,Y)$ where $X,Y$ follows a bivariate normal distribution. 

Then
$$f_{\mathbf{Z}}(z)= \frac{1}{2\pi \sqrt{ \det(\Sigma) }}\exp \left\{  -\frac{1}{2}(z- \mu)^T \Sigma^{-1}(z-\mu)  \right\}$$
where $\mu=(\mu_{X},\mu_{Y})$ and $\Sigma$ is the [[6 - Main Notes/variance-covariance matrix\|variance-covariance matrix]] of $\mathbf{Z}$.

##### Proof
First we have
$$\det \Sigma=(1-\rho^2)(\sigma_{X}^2\sigma_{Y}^2).$$

Now
$$\Sigma^{-1}=\frac{1}{(1-\rho^2)(\sigma_{X}^2 \sigma_{Y}^2)} \begin{bmatrix}
\sigma_{Y}^2 & -\rho \sigma_{X}\sigma_{Y} \\
-\rho \sigma_{X}\sigma_{Y} & \sigma_{X}^2
\end{bmatrix}.$$
Observe
$$\begin{align}
(z-\mu)^T \Sigma^{-1}(z-\mu) &= \frac{1}{(1-\rho^2)(\sigma_{X}^2\sigma_{Y}^2)} (x-\mu_{X}, y - \mu_{Y}) \begin{pmatrix}
\sigma_{Y}^2 & -\rho \sigma_{X}\sigma_{Y} \\
-\rho \sigma_{X}\sigma_{Y} & \sigma_{X}^2
\end{pmatrix} \begin{pmatrix}
x - \mu_{X} \\
y-\mu_{Y}
\end{pmatrix}  \\
&=  \frac{1}{1-\rho^2} (x-\mu_{X}, y - \mu_{Y}) \begin{pmatrix}
\left(\frac{x-\mu_{X}}{\sigma_{X}^2}\right) -\rho\left(\frac{y-\mu_{Y}}{\sigma_{X}\sigma_{Y}}\right) \\
-\rho\left(\frac{x-\mu_{X}}{\sigma_{X}\sigma_{Y}}\right) + \left(\frac{y-\mu_{Y}}{\sigma_{Y}^2}\right)
\end{pmatrix} \\
&= \frac{1}{1-\rho^2} \left[\left(\frac{x-\mu_{X}}{\sigma_{X}}\right)^2-2\rho \left(\frac{x-\mu_{X}}{\sigma_{X}}\right)\left(\frac{y-\mu_{Y}}{\sigma_{Y}}\right)+ \left(\frac{y-\mu_{Y}}{\sigma_{Y}}\right)^2\right]
\end{align}$$
and we are done.

##### Notation

Write this as
$$\mathbf{Z} \sim \mathcal{N}(\mu, \Sigma).$$

### Construction
+ [[6 - Main Notes/Construction of the bivariate normal distribution\|Construction of the bivariate normal distribution]]