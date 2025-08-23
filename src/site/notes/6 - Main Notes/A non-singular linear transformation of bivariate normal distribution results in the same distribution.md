---
{"dg-publish":true,"permalink":"/6-main-notes/a-non-singular-linear-transformation-of-bivariate-normal-distribution-results-in-the-same-distribution/","tags":["probability_theory","info"]}
---

### Statement

Suppose $T:\mathbb{R}^2 \rightarrow \mathbb{R}^2$ is a non-singular linear transform and suppose $\mathbf{X}=(X_{1},X_{2})$ follows a [[6 - Main Notes/Bivariate normal distribution\|bivariate normal distribution]], i.e., $\mathbf{X} \sim \mathcal{N}_{2}(\bar{\mu},\Sigma)$.

Then $$\mathbf{Y}=T(\mathbf{X}) \sim \mathcal{N}_{2}(\begin{pmatrix}
A\bar{\mu}, A \Sigma A^T
\end{pmatrix})$$
where $A$ is the matrix representation of the linear transform, i.e., $T(\mathbf{X})=A\mathbf{X}$.

### Proof

Define the function $h:\mathbb{R}^2 \rightarrow \mathbb{R}^2$ by
$$h(x_{1},x_{2})= \begin{pmatrix}
a_{11}x_{1} + a_{12}x_{2} \\
a_{21}x_{1} + a_{22}x_{2}
\end{pmatrix}=A \mathbf{x}=\mathbf{y}.$$
Note that 
$$h^{-1}(y_{1},y_{2})=A^{-1}\mathbf{y}.$$
Also note that
$$J = \det \begin{pmatrix}
\frac{\partial h_{1}}{\partial x_{1}} & \frac{\partial h_{1}}{\partial x_{2}} \\
\frac{\partial h_{2}}{\partial x_{1}} & \frac{\partial h_{2}}{\partial x_{2}}
\end{pmatrix} = \det\begin{pmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{pmatrix} = \det A.$$
The joint pdf of $(Y_{1},Y_{2})=(a_{11}X_{1}+a_{22}X_{2},a_{21}X_{1}+a_{22}X_{2})$ is given by
$$\begin{align}
f_{\mathbf{Y}}(\mathbf{y})&= f_{\mathbf{X}}(h^{-1}(\mathbf{y}))\cdot |J|^{-1}\\
&= \frac{1}{2\pi (\det A) }\exp\left\{  -\frac{1}{2}(A^{-1}\mathbf{y}- \bar{\mu})^T  \Sigma^{-1}(A^{-1}\mathbf{y}- \bar{\mu})\right\} \\
&= \frac{1}{2\pi \sqrt{ \det(A \Sigma A^T) }}\exp\left\{  -\frac{1}{2}[A^{-1}(\mathbf{y}-A \bar{\mu})]^T \Sigma^{-1}[A^{-1}(\mathbf{y}-A\bar{\mu})] \right\} \\
&=\frac{1}{2\pi \sqrt{ \det(A \Sigma A^T) }}\exp\left\{  -\frac{1}{2}(\mathbf{y}-A \bar{\mu})^T(A^{-1})^T \Sigma^{-1}A^{-1}(\mathbf{y}-A\bar{\mu}) \right\} \\
&=\frac{1}{2\pi \sqrt{ \det(A \Sigma A^T) }}\exp\left\{  -\frac{1}{2}(\mathbf{y}-A \bar{\mu})^T (A^{-1}\Sigma^{-1}A^{T})^{-1}(\mathbf{y}-A\bar{\mu}) \right\} \\
&\equiv \mathcal{N}_{2}(A\bar{\mu}, A\Sigma A^T).
\end{align}$$


