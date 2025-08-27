---
{"dg-publish":true,"permalink":"/6-main-notes/assignment-2-problem-3-rotation-of-bivariate-normal-variables-by-an-angle-that-causes-independence/","tags":["probability_theory","problem"]}
---

### Problem

Suppose $(X,Y)$ are bivariate normal random variables with $\mu_{X}=\mu_{Y}=0$ and variance $\sigma_{X}^2,\sigma_{Y}^2$ respectively. 

Show that if 
$$\theta=\frac{1}{2}\cot^{-1}\left(\frac{\sigma_{X}^2-\sigma_{Y}^2}{2\rho \sigma_{X}\sigma_{Y}}\right)$$
then $X\cos \theta+Y\sin \theta$ and $Y\cos \theta-X\sin \theta$ are two independent random variables.

### Solution

Consider the function $T:\mathbb{R}^2 \rightarrow \mathbb{R}^2$ defined by
$$\begin{align}
T\begin{pmatrix}
X \\
Y
\end{pmatrix} &= \begin{pmatrix}
X\cos \theta+Y \sin \theta \\
Y\cos \theta-X\sin \theta
\end{pmatrix}  \\
&= \begin{pmatrix}
\cos \theta & \sin \theta \\
-\sin \theta & \cos \theta
\end{pmatrix} \begin{pmatrix}
X \\
Y
\end{pmatrix}.
\end{align}$$
Note that $T$ is linear and non-singular and thus, $Z_{1}=X\cos \theta+Y\sin \theta$ and $Z_{2}=Y\cos \theta-X\sin \theta$ are jointly normal.

Note that we have
$$\cot 2\theta = \frac{\sigma_{X}^2-\sigma_{Y}^2}{2\rho \sigma_{X}\sigma_{Y}}.$$
Also,
$$\begin{align}
\frac{\cos 2\theta}{\sin 2\theta} + \frac{\sin 2\theta}{\cos 2\theta} &= \frac{1}{\sin 2\theta \cos 2\theta}  \\
&= \frac{\sigma_{X}^2-\sigma_{Y}^2}{2\rho \sigma_{X}\sigma_{Y}}+ \frac{2\rho \sigma_{X}\sigma_{Y}}{\sigma_{X}^2- \sigma_{Y}^2} \\
&= \frac{(\sigma_{X}^2-\sigma_{Y}^2)^2+ (2\rho \sigma_{X}\sigma_{Y})^2}{2\rho \sigma_{X}\sigma_{Y}(\sigma_{X}^2-\sigma_{Y}^2)}.
\end{align}$$
Thus,
$$\begin{align}
\cot 2\theta\sin 2\theta \cos 2\theta &= \cos^2 2\theta \\
&= \left(\frac{\sigma_{X}^2-\sigma_{Y}^2}{2\rho \sigma_{X}\sigma_{Y}}\right)\left( \frac{2\rho \sigma_{X}\sigma_{Y}(\sigma_{X}^2-\sigma_{Y}^2)}{(\sigma_{X}^2-\sigma_{Y}^2)^2 + (2\rho \sigma_{X}\sigma_{Y})^2} \right) \\
&= \frac{(\sigma_{X}^2-\sigma_{Y}^2)^2}{(2\rho \sigma_{X}\sigma_{Y})^2+(\sigma_{X}^2+\sigma_{Y}^2)^2}.
\end{align}$$
Now we compute
$$\begin{align}
\sin^2 2\theta &= 1 - \cos^2 2\theta \\
&= \frac{(2\rho \sigma_{X}\sigma_{Y})^2}{(2\rho \sigma_{X}\sigma_{Y})^2 + (\sigma_{X}^2+\sigma_{Y}^2)^2}.
\end{align}$$
The correlation between $Z_{1}$ and $Z_{2}$ is given by
$$\begin{align}
\rho_{Z_{1},Z_{2}} &= \frac{\text{Cov}(X\cos \theta+Y \sin \theta, Y\cos \theta - X \sin \theta)}{\sigma_{Z_{1}}\sigma_{Z_{2}}}.
\end{align}$$
The numerator is
$$
\rho \sigma_{X}\sigma_{Y}\cos^2\theta+(\sigma^2_{Y}-\sigma^2_{X})\sin \theta \cos \theta - \rho \sigma_{X}\sigma_{Y}\sin^2 \theta = \rho \sigma_{X}\sigma_{Y}\cos 2\theta+ (\sigma_{Y}^2- \sigma_{X}^2)\frac{\sin 2\theta}{2}$$
but the expression at the right is
$$\rho \sigma _{X}\sigma_{Y}\frac{\sigma^2_{X}-\sigma_{Y}^2}{\sqrt{ (2\rho \sigma_{X}\sigma_{Y})^2 + (\sigma_{X}^2-\sigma_{Y}^2)^2 }}-(\sigma_{Y}^2-\sigma_{X}^2) \frac{\rho \sigma_{X}\sigma_{Y}}{\sqrt{ (2\rho \sigma_{X}\sigma_{Y})^2 + (\sigma_{X}^2-\sigma_{Y}^2)^2 }}=0.$$

Since $\rho_{Z_{1},Z_{2}}=0$ and $Z_{1},Z_{2}$ are jointly normal, we conclude that $Z_{1},Z_{2}$ are independent. 