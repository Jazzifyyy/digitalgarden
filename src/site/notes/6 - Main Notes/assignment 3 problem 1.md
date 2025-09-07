---
{"dg-publish":true,"permalink":"/6-main-notes/assignment-3-problem-1/","tags":["probability_theory","problem"]}
---

### Problem

Suppose $X_{1},\dots,X_{n}$ are iid standard normal variables. Let $\mathbf{X}$ be a random vector, i.e., 
$$\mathbf{X}:= \begin{pmatrix}
X_{1} \\
\vdots \\
X_{d}
\end{pmatrix}$$
and let $A$ be a $d \times d$ *non-singular* matrix with real entries.

Define $\mathbf{Y}:= A\mathbf{X}$. Show that $\mathbf{Y}$ is a *multivariate normal random vector* with *mean vector* $\mathbf{0}$ and *variance-covariance matrix* $AA^T$.

### Solution

Define $h:\mathbb{R}^d \rightarrow \mathbb{R}^d$ by
$$h(\mathbf{x})= A\mathbf{x}=\begin{pmatrix}
a_{11} & a_{12} & \dots & a_{1d} \\
\vdots & & &\vdots\\
a_{d1} & a_{d 2} & \dots & a_{dd}
\end{pmatrix}\begin{pmatrix}
x_{1} \\
\vdots \\
x_{d}
\end{pmatrix}=\begin{pmatrix}
a_{11}x_{1}+a_{12}x_{2}+\dots+ a_{1 d}x_{d} \\
\vdots \\
a_{d 1}x_{1} + a_{d_{2}}x_{2}+\dots+ a_{dd}x_{d}
\end{pmatrix}.$$
Note that $h^{-1}(\mathbf{y})=A^{-1}\mathbf{y}$ and
$$J = \det \begin{pmatrix}
\frac{\partial h_{1}}{\partial x_{1}} & \frac{\partial h_{1}}{\partial x_{2}} & \dots &  \frac{\partial h_{1}}{\partial x_{d}}\\ 
\vdots \\
\frac{\partial h_{d}}{\partial x_{1}} & \frac{\partial h_{d}}{\partial x_{2}} & \dots & \frac{\partial h_{d}}{\partial x_{d}}
\end{pmatrix} = \det A.$$
The joint pdf of $\mathbf{Y}=A\mathbf{X}$ is given by
$$
\begin{align}
f_{\mathbf{Y}}(\mathbf{y}) &= f_{\mathbf{X}}(h^{-1}(\mathbf{y})). |J|^{-1} \\
&= \frac{1}{2\pi \sqrt{ \det I }}\exp \left\{  -\frac{1}{2}[(h^{-1}(\mathbf{y})-\mathbf{0})^TI(h^{-1}(\mathbf{y})-\mathbf{0})]  \right\}. \left|\frac{1}{\det A}\right| \\
&= \frac{1}{2\pi \sqrt{ \det (AA^T) }}\exp \left\{  -\frac{1}{2}(A^{-1}\mathbf{y})^T(A^{-1}\mathbf{y})   \right\} \\
&= \frac{1}{2\pi \sqrt{ \det (AA^T) }}\exp \left\{  -\frac{1}{2}\mathbf{y}^T(AA^T)^{-1}\mathbf{y})   \right\}
\end{align}.
$$
The last equality is true because $(A^{-1})^TA^{-1}=(A^T)^{-1}A^{-1}=(AA^T)^{-1}$.

Thus $\mathbf{Y}$ follows a multivariate normal distribution with mean $\mathbf{0}$ and variance-covariance matrix $AA^T$.
 