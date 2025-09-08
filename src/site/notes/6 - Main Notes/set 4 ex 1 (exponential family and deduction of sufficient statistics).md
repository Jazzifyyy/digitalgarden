---
{"dg-publish":true,"permalink":"/6-main-notes/set-4-ex-1-exponential-family-and-deduction-of-sufficient-statistics/","tags":["inference","problem"]}
---

(Recall: [[6 - Main Notes/one-parameter exponential family\|one-parameter exponential family]], [[6 - Main Notes/multiparameter exponential family\|multiparameter exponential family]])
### Problem

Check whether the following distributions belong to the exponential family. If so, then identify a minimal statistic for the unknown parameters. 

1. $f_{\theta}=\text{Laplace}(a,b), \theta=(a,b)$.
2. $f_{\theta}= \text{Beta}(\alpha, \beta), \theta = (\alpha, \beta)$.

### Solution
 
##### Part 1.

A random variable has a $\text{Laplace}(a,b)$ distribution, where $a \in \mathbb{R}$ and $b>0$, iff its pdf is given by
$$f_{(\mu,b)}(x)=\frac{1}{2b}\exp \left\{ - \frac{|x-a|}{b} \right\}.$$
for $x \in \mathbb{R}$.

If $a=0$, then the pdf becomes $\exp \left\{  - \frac{|x|}{b} - \log2b  \right\}$ with $c(x)=1$, $a(\theta)=-\frac{1}{b}$, $\tau(x)=|x|$, $b(\theta)=-\log 2b$. Thus $\text{Laplace}(0, \theta)$ belong to the [[6 - Main Notes/one-parameter exponential family\|one-parameter exponential family]].

A minimal statistic for $b$ is $\sum_{i=1}^n |X_{i}|$.


If $a \neq 0$, then the laplace distribution does not belong to the exponential family.

##### Part 2.

We have
$$f_{\theta}(x)= \frac{1}{\beta(\alpha, \beta)}x^{\alpha-1}(1-x)^{\beta-1}= \frac{1}{\beta(\alpha, \beta)}\exp \{ (\alpha-1)\log x+(\beta-1)\log(1-x) \}$$
where $x \in (0,1)$.

This belong to the two-parameter exponential family with $c(x)=\frac{1}{\beta(\alpha, \beta)}$, $a_{1}(\theta)=\alpha-1$, $\tau_{1}(x)=\log x$, $a_{2}(\theta)=\beta-1$, $\tau_{2}(x)= \log(1-x)$.

Thus, a minimal statistic for $(\alpha, \beta)$ is
$$\left( \sum_{i=1}^n \log X_{i}, \sum_{i=1}^n \log(1-X_{i}) \right)= \left( \log \prod_{i=1}^n X_{i}, \log \prod_{i=1}^n (1 - X_{i})\right)\equiv \left( \prod_{i=1}^n X_{i}, \prod_{i=1}^n (1-X_{i}) \right).$$