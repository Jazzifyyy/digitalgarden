---
{"dg-publish":true,"permalink":"/6-main-notes/assignment-1-problem-2-independent-normals-bivariate-normals-and-conditional-distributions/","tags":["probability_theory","problem"]}
---

### Problem

Suppose $X,Y$ are independent standard normal variables.

1. For a constant $k$, find $\mathbb{P}(X>kY)$.
2. If $U= \sqrt{ 3 }X+Y$ and $V= X - \sqrt{ 3 }Y$, find $\mathbb{P}(U>kV)$.
3. Find $\mathbb{P}(U^2+V^2<1)$.
4. Find the conditional distribution of $X$ given $V=v$.

### Solution

##### Part 1

Since $X,Y$ are independent, we have $X-kY \sim \mathcal{N}(0,1+k^2)$, and thus
$$\begin{align}
\mathbb{P}(X>kY) &= \mathbb{P}(X-kY>0) \\
&= \frac{1}{2}.
\end{align}$$

##### Part 2

Define $T:\mathbb{R}^2 \rightarrow \mathbb{R}^2$ by
$$T\left(\begin{pmatrix}
X \\
Y
\end{pmatrix}\right)=\begin{pmatrix}
\sqrt{ 3 }X+Y  \\
X-\sqrt{ 3 }Y
\end{pmatrix} =\begin{pmatrix}
\sqrt{ 3 } & 1 \\
1 & -\sqrt{ 3 }
\end{pmatrix} \begin{pmatrix}
X \\
Y
\end{pmatrix}.$$
$T$ is non-singular and linear, and thus $U,V$ are jointly normal.

But
$$\begin{align}
\text{Cov}(\sqrt{ 3 }X + Y, X-\sqrt{ 3 }Y) &= \sqrt{ 3 }\text{Cov}(X,X)-3\text{Cov}(X,Y)+\text{Cov}(Y,X)-\sqrt{ 3 } \text{Cov}(Y,Y)\\ &=\sqrt{ 3 }-0+0-\sqrt{ 3 } \\
&= 0.
\end{align}$$
and thus $U=\sqrt{ 3 }X+Y \sim \mathcal{N}(0,4)$ and $V=X-\sqrt{ 3 }Y \sim \mathcal{N}(0,4)$ are independent normal distributions. 

Therefore, $U-kV\sim \mathcal{N}(0,4+k^24)$ with
$$\begin{align}
\mathbb{P}(U>kV) &= \mathbb{P}(U-kV>0) \\
&= \frac{1}{2}.
\end{align}$$
##### Part 3

Since $\frac{U}{2}, \frac{V}{2}$ are standard normal distributions, we have $\frac{U^2}{4} + \frac{V^2}{4} \sim \chi^2_{2}$.

Thus,
$$\mathbb{P}(U^2+V^2 < 1)=\mathbb{P}\left( \frac{U^2}{4} + \frac{V^2}{4}< \frac{1}{4}\right) \approx 0.11750.$$
##### Part 4

Define $T:\mathbb{R}^2 \rightarrow \mathbb{R}^2$ by
$$T\left(\begin{pmatrix}
X \\
Y
\end{pmatrix}\right) = \begin{pmatrix}
X \\
X-\sqrt{ 3 }Y
\end{pmatrix} = \begin{pmatrix}
1 & 0 \\
1 & -\sqrt{ 3 }
\end{pmatrix}\begin{pmatrix}
X \\
Y
\end{pmatrix}.$$
Note that $T$ is non-singular and linear, and thus $X,V$ are jointly normal.

Also
$$\text{Cov}(X,X- \sqrt{ 3 }Y) = \text{Cov}(X,X) -\sqrt{ 3 }\text{Cov}(X,Y)=1$$
and
$$\rho= \frac{\text{Cov}(X,V)}{\sigma_{X}\sigma_{V}}= \frac{1}{2}.$$

Thus,
$$\begin{pmatrix}
X \\
V
\end{pmatrix} \sim \mathcal{N}_{2}\left( \begin{pmatrix}
0 \\
0
\end{pmatrix}, \begin{pmatrix}
1 & 1 \\
1 & 4
\end{pmatrix} \right).$$

We have
$$\begin{align}
f_{X|V=v}(x|v) &= \frac{f_{X,V}(x,v)}{f_{V}(v)} \\ \\
&= \frac{\frac{1}{2\pi \sigma_{X}\sigma_{V}\sqrt{ 1-\rho^2 }}\exp\left\{ -\frac{1}{2(1-\rho^2)}\left[\left(\frac{x-\mu_{X}}{\sigma_{X}}\right)^2+ \left(\frac{v - \mu_{V}}{\sigma_{V}}\right)^2- 2\rho \left(\frac{x-\mu_{X}}{\sigma_{X}}\right)\left(\frac{v-\mu_{V}}{\sigma_{V}}\right)\right] \right\}}{\frac{1}{\sigma_{V}\sqrt{ 2\pi }}\exp\left\{  -\frac{1}{2}\left(\frac{v-\mu_{V}}{\sigma_{V}}\right)^2  \right\}} \\
&=\frac{1}{\sqrt{ 2\pi(1-\rho^2) }\sigma_{X}}\exp\left\{  -\frac{1}{2(1-\rho^2)}\left[\rho^2\left(\frac{v-\mu_{V}}{\sigma_{V}}\right)^2 -2\rho\left(\frac{x-\mu_{X}}{\sigma_{X}}\right)\left(\frac{v-\mu_{V}}{\sigma_{V}}\right)+\left(\frac{x-\mu_{X}}{\sigma_{X}}\right)^2\right]  \right\}  \\
&= \frac{1}{\sqrt{ 2\pi (1-\rho^2) }\sigma_{X}}\exp\left\{  - \frac{1}{2(1-\rho^2)\sigma_{X}^2} \left[x-\left(\mu_{X}+ \rho \sigma_{X}\frac{v-\mu_{V}}{\sigma_{V}}\right)\right]^2 \right\} \\
&\equiv \mathcal{N}\left( \mu_{X}+ \frac{\rho \sigma_{X}}{\sigma_{V}}(v-\mu_{V}),\sigma_{X}^2(1-\rho^2) \right) \\
&\equiv \mathcal{N}\left( \frac{v}{4}, \frac{3}{4} \right).
\end{align}$$
