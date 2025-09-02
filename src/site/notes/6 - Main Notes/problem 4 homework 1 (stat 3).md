---
{"dg-publish":true,"permalink":"/6-main-notes/problem-4-homework-1-stat-3/","tags":["regression","problem"]}
---

### Problem

Suppose you have fitted a regression line $Y=b_{0}+b_{1}X$ on $n$ pairs of observations where $b_{0}$ and $b_{1}$ are the least square estimators. For a new value $x_{0}$ of $X$, what is the predicted value of $Y$? What is the variance of the prediction? How does the variance depend on $x_{0}$? Interpret this result.

### Solution

For a new value $x_{0}$ of $X$, the predicted value of $Y$ is $b_{0}+b_{1}x_{0}$ with variance $0$, since $b_{0}+b_{1}x_{0}$ is not random. Thus, the variance of the prediction does not depend on $x_{0}$.

Given $n$ pairs of observations, once we obtain $b_{0}$ and $b_{1}$, our model deterministically predicts $y$ given a new value of $x$.

Note that
$$\begin{align}
\sum_{i=1}^n (x_{i}-\bar{x})(y_{i}-\bar{y}) &= \sum_{i=1}^n (x_{i}-\bar{x})y_{i} - \sum_{i=1}^n (x_{i}-\bar{x})\bar{y} \\
&= \sum_{i=1}^n (x_{i}-\bar{x})y_{i} - \bar{y}(n\bar{x}-n\bar{x}) \\
&= \sum_{i=1}^n (x_{i}-\bar{x})(\beta_{0}+\beta_{1}x_{i} + e_{i}).
\end{align}$$
The variance of the estimate of the slope is given by 
$$\begin{align}
\text{Var}(b_{1}) &= \text{Var}\left( \frac{\sum_{i=1}^n (x_{i}-\bar{x})(y_{i}-\bar{y})}{\sum_{i=1}^n (x_{i}-\bar{x})^2} \right) \\
&= \text{Var}\left( \frac{\sum_{i=1}^n (x_{i}-\bar{x})(\beta_{0}+\beta_{1}x_{i}+e_{i})}{} \right)
\end{align}$$
...

We have $\text{Var}(b_{1})= \frac{\sigma^2}{\sum_{i=1}^n (x_{i}-\bar{x})^2}$ and $$\text{Var}(b_{0})= \sigma^2\left( \frac{1}{n}+ \frac{\bar{x}^2}{\sum_{i=1}^n (x_{i}-\bar{x})^2} \right).$$
The variance of the prediction is
$$\begin{align}
\text{Var}(b_{0}+b_{1}x_{0}) &= \text{Var}(b_{0})+ x_{0}^2 \text{Var}(b_{1}) + 2x_{0} \text{Cov}(b_{0},b_{1}) \\
&= \sigma^2\left( \frac{1}{n} + \frac{\bar{x}^2}{\sum_{i=1}^n (x_{i}-\bar{x})^2} \right) + \frac{x_{0}^2\sigma^2}{\sum_{i=1}^n (x_{i}-\bar{x})^2} + 2x_{0}\left( -\frac{\sigma^2\bar{x}}{\sum_{i=1}^n (x_{i}-\bar{x})^2} \right) \\
&= \frac{\sigma^2}{n} + \frac{\sigma^2}{\sum_{i=1}^n (x_{i}-\bar{x})^2}(\bar{x}^2+x_{0}^2 -2x_{0}\bar{x}) \\
&= \sigma^2\left( \frac{1}{n}+(x_{0}-\bar{x})^2 \right).
\end{align}$$

