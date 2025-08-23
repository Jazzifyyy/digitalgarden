---
{"dg-publish":true,"permalink":"/6-main-notes/assignment-1-problem-4-expectation-of-max-of-standard-bivariate-normals/","tags":["probability_theory","problem"]}
---

### Problem

Show that for standard bivariate normal variables $X$ and $Y$ with correlation $\rho$, we have
$$\mathbb{E}[\max(X,Y)] = \sqrt{ \frac{1-\rho}{\pi} }.$$
### Solution

Note the following:
$$\begin{align}
\max(X,Y) &= X. \mathbb{1}_{\{ X>Y \}} + Y.\mathbb{1}_{\{ Y>X \}} \\
&= X.(1 - \mathbb{1}_{\{ Y>X \}})+ Y. \mathbb{1}_{\{ Y>X \}}  \\
&= X +(Y-X). \mathbb{1}_{\{ Y-X> 0\}}.
\end{align}$$
Define $Z:=Y-X$ where $\mathbb{E}[Z]=\mathbb{E}[Y]-\mathbb{E}[X]=0$ and $\text{Var}(Z)=\text{Var}(Y)+ \text{Var}(X) - 2 \text{Cov}(Y,X)=2(1-\rho)$.

Thus, $Z \sim \mathcal{N}(0, 2(1-\rho))$.

Finally, $$\mathbb{E}[\max(X,Y)]= \mathbb{E}[X]+\mathbb{E}[Z.\mathbb{1}_{\{ Z>0 \}}]= \sqrt{ \frac{1-\rho}{\pi} }$$
where we solved
$$\begin{align}
I=\int_{0}^\infty \frac{1}{\sqrt{ 4\pi(1-\rho) }}ze^{-z^2/(4(1-\rho))}dz
\end{align}$$
by taking $t=-\frac{z^2}{4(1-\rho)}$ with $-2(1-\rho)dt=zdz$ yielding: 
$$I= -\sqrt{ \frac{1-\rho}{\pi} }\int_{0}^{-\infty}e^tdt= \sqrt{ \frac{1-\rho}{\pi} }.$$
