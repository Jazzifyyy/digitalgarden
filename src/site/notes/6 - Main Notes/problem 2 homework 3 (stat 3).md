---
{"dg-publish":true,"permalink":"/6-main-notes/problem-2-homework-3-stat-3/","tags":["regression","problem"]}
---

The estimates of $Y$ on $X$ is $(\hat{\beta}_{0}, \hat{\beta}_{1})=(22,-3)$ and the estimates of $X$ on $Y$ is $(\hat{\alpha}_{0}, \hat{\alpha}_{1})=(5.84,-0.12)$. 

Then we have $\hat{\alpha}_{0}=\bar{x}-\hat{\alpha}_{1}\bar{y}$ and $\hat{\beta}_{0}=\bar{y}-\hat{\beta}_{1}\bar{x}$. 

Substituting the second in the first:
$$\begin{align*}
\hat{\alpha}_{0} &= \bar{x} - \hat{\alpha}_{1}(\hat{\beta}_{0}+\hat{\beta}_{1}\bar{x})\\
&= (1-\hat{\alpha}_{1}\hat{\beta}_{1})\bar{x}-\hat{\alpha}_{1}\hat{\beta}_{0}\\
\end{align*}$$
and thus, 
$$\bar{x}=\frac{\hat{\alpha}_{0}+\hat{\alpha}_{1}\hat{\beta}_{0}}{1- \hat{\alpha}_{1}\hat{\beta}_{1}}=\frac{5.84+(-0.12)(22)}{1- (-0.12)(-3)}= 5.$$
Now we can find
$$\bar{y}=\hat{\beta}_{0}+\hat{\beta}_{1}\bar{x}=22+(-3)(5)=7.$$
The sample correlation is given by
$$\hat{\alpha}_{1}\hat{\beta}_{1}=r^2=(-3)(-0.12)=0.36$$
and thus, the sample correlation is $r = -0.6$. We conclude that it is negative by observing the following expression:
$$\hat{\beta}_{1}= r. \frac{S_{x}}{S_{y}},$$
since $\hat{\beta}_{1}$ is negative and $S_{x}$ and $S_{y}$ are positive.

Using the same expression,
$$\frac{S_{x}^2}{S_{y}^2}= \frac{\hat{\beta}_{1}^2}{r^2}=\frac{(0.12)^2}{(0.6)^2}=0.04.$$
