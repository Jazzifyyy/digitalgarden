---
{"dg-publish":true,"permalink":"/6-main-notes/standard-bivariate-normal-distribution/","tags":["info","probability_theory"]}
---

### Definition

Two random variables $X$ and $Y$ are said to have the **standard bivariate normal distribution** with correlation coefficient $\rho$ if their joint pdf is given by
$$f_{X,Y}(x,y)= \frac{1}{2\pi \sqrt{ 1- \rho^2 }}\exp \left\{  -\frac{x^2 -2 \rho xy + y^2}{2(1- \rho^2)}  \right\}$$
where $\rho \in (-1,1)$.

### Notation

Write this as
$$(X,Y) \sim \mathcal{N}_{2}\left(\begin{pmatrix}0 \\ 0 \end{pmatrix}, \begin{pmatrix}
1 & \rho  \\
\rho & 1
\end{pmatrix}\right).$$
The matrix in the second argument is the [[6 - Main Notes/variance-covariance matrix\|variance-covariance matrix]].

### Construction
+ [[6 - Main Notes/Construction of the standard bivariate normal distribution\|Construction of the standard bivariate normal distribution]]