---
{"dg-publish":true,"permalink":"/6-main-notes/problem-1-homework-1-stat-3/","tags":["regression","info"]}
---

### Problem

Consider a linear regression model
$$y_{i}=\alpha+\beta x_{i}+e_{i}$$
where $i\in \{ 1,\dots,n \}$, $x_{i}$'s are fixed and $e_{i}$'s are independent random errors with mean $0$ and variance $\sigma^2$. Define two estimators of $\beta$ as follows:
$$\hat{\beta}_{1}= \frac{\sum_{i=1}^n y_{i}}{\sum_{i=1}^n x_{i}} \text{ and }\hat{\beta}_{2}= \frac{\sum_{i=1}^nx_{i}y_{i}}{\sum_{i=1}^n x_{i}^2}.$$
1. Obtain an unbiased estimator of $\beta$ as a linear combination of $\hat{\beta}_{1}$ and $\hat{\beta}_{2}$.
2. Find the mean squared errors of $\hat{\beta}_{1}$ and $\hat{\beta}_{2}$.

### Solution

##### Part 1

We have
$$\begin{align}
\mathbb{E}[\hat{\beta}_{1}] &= \mathbb{E}\left[ \frac{\sum_{i=1}^n (\alpha+\beta x_{i}+ e_{i})}{\sum_{i=1}^n x_{i}} \right]  \\
&= \frac{n\alpha}{\sum_{i=1}^n x_{i}} + \beta+ \frac{1}{\sum_{i=1}^nx_{i}}\sum_{i=1}^n\mathbb{E}[e_{i}]  \\
&= \beta + \frac{n\alpha}{\sum_{i=1}^n x_{i}}
\end{align}$$
and
$$\begin{align}
\mathbb{E}[\hat{\beta}_{2}] &= \mathbb{E}\left[ \frac{\sum_{i=1}^n x_{i}(\alpha+\beta x_{i}+e_{i})}{\sum_{i=1}^n x_{i}^2}\right] \\
&= \alpha\frac{\sum_{i=1}^n x_{i}}{\sum_{i=1}^n x_{i}^2} + \beta+ \frac{1}{\sum_{i=1}^nx_{i}^2}\mathbb{E}[e_{i}] \\
&= \beta + \frac{\alpha\sum_{i=1}^nx_{i}}{\sum_{i=1}^n x_{i}^2}.
\end{align}$$
The expectation of a linear combination of $\hat{\beta}_{1}$ and $\hat{\beta}_{2}$ is
$$\mathbb{E}[a\hat{\beta}_{1}+b \hat{\beta}_{2}] = \beta(a+b)+a \frac{n\alpha}{\sum_{i=1}^n x_{i}} + b \frac{\alpha \sum_{i=1}^n x_{i}}{\sum_{i=1}^n x_{i}^2}.$$
This is equal to $\beta$ iff $b=1-a$ and 
$$\begin{align}
&a \frac{n\alpha}{\sum_{i=1}^n x_{i}} + b \frac{\alpha \sum_{i=1}^n x_{i}}{\sum_{i=1}^n x_{i}^2} = 0 \\
&\iff a \frac{n\alpha}{\sum_{i=1}^n x_{i}} + (1-a) \frac{\alpha \sum_{i=1}^n x_{i}}{\sum_{i=1}^n x_{i}^2}=0 \\
&\iff a \left[ \frac{n\alpha}{\sum_{i=1}x_{i}}- \frac{\alpha \sum_{i=1}^n x_{i}}{\sum_{i=1}^n x_{i}^2} \right] =-\frac{\alpha \sum_{i=1}^n x_{i}}{\sum_{i=1}^n x_{i}^2} \\
&\iff a = \frac{-\frac{\sum x_{i}}{\sum x_{i}^2}}{\frac{n \sum x_{i}^2}{\sum x_{i}\sum x_{i}^2}- \frac{\sum x_{i}}{\sum x_{i}^2}} \\
&\iff a = \frac{-\left( \sum_{i=1}^n x_{i} \right)^2}{n \sum_{i=1}^n x_{i}^2 - \left( \sum_{i=1}^n x_{i} \right)^2}.
\end{align}$$
Thus, the required estimator is
$$\left[\frac{-\left( \sum_{i=1}^n x_{i} \right)^2}{n \sum_{i=1}^n x_{i}^2 - \left( \sum_{i=1}^n x_{i} \right)^2}\right]\hat{\beta}_{1}+ \left[ \frac{n\sum_{i=1}^n x_{i}^2}{n\sum_{i=1}^n x_{i}^2 - \left( \sum_{i=1}^n x_{i} \right)^2} \right]\hat{\beta}_{2}.$$
##### Part 2

We have
$$\begin{align}
\text{MSE}_{\beta}(\hat{\beta}_{1})&= \text{Var}(\hat{\beta}_{1})+ B_{\beta}^2(\hat{\beta}_{1}) \\
&= \frac{1}{\left( \sum_{i=1}^n x_{i} \right)^2}\text{Var}\left[ n\alpha+\beta\sum_{i=1}^nx_{i}+\sum_{i=1}^n e_{i} \right]+\left( \beta + \frac{n\alpha}{\sum_{i=1}^n x_{i}} - \beta\right)^2 \\
&= \frac{n\sigma^2}{\left( \sum_{i=1}^n x_{i} \right)^2} + \left( \frac{n\alpha}{\sum_{i=1}^n x_{i}} \right)^2 \\
&= \frac{n^2\alpha^2+n\sigma^2}{\left( \sum_{i=1}^n x_{i} \right)^2}
\end{align}$$
and
$$\begin{align}
\text{MSE}_{\beta}(\hat{\beta}_{2})&= \text{Var}(\hat{\beta}_{2})+ B_{\beta}^2(\hat{\beta}_{2}) \\
&= \frac{1}{\left( \sum_{i=1}^n x_{i}^2 \right)^2}\text{Var}\left[ \alpha \sum_{i=1}^n x_{i}+\beta \sum_{i=1}^n x_{i}^2+\sum_{i=1}^n x_{i}e_{i} \right]+\left( \beta + \frac{\alpha \sum_{i=1}^n x_{i}}{\sum_{i=1}^n x_{i}^2} - \beta\right)^2 \\
&= \frac{\sigma^2\sum_{i=1}^n x_{i}^2}{\left( \sum_{i=1}^n x_{i}^2 \right)^2} + \left( \frac{\alpha \sum_{i=1}^n x_{i}}{\sum_{i=1}^n x_{i}^2} \right)^2 \\
&= \frac{\alpha^2\left( \sum_{i=1}^nx_{i} \right)^2 + \sigma^2\sum_{i=1}^n x_{i}^2}{(\sum_{i=1}^n x_{i}^2)^2}.
\end{align}$$
