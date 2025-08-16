---
{"dg-publish":true,"permalink":"/6-main-notes/assignment-1-problem-1-normal-and-bivariate-normal/","tags":["probability_theory","problem"]}
---

### Problem

Suppose $X$ and $Y$ are two standard normal variables. Find an expression for $\mathbb{P}(X+2Y\leq 3)$ in terms of the standard normal distribution function, when
1. $X$ and $Y$ are independent.
2. $X$ and $Y$ have bivariate normal distribution with correlation $\frac{1}{2}$.
### Solution

##### Part 1

Note that 
$$\begin{align*}
\mathbb{E}[X+2Y] &= \mathbb{E}[X]+2 \mathbb{E}[Y] \\
&= 0 + 2.0 \\
&= 0
\end{align*}$$
and
$$\begin{align*}
\text{Var}(X+2Y) &= \text{Var}(X)+4 \text{Var}(Y) \\
&= 1 + 4.1 \\
&= 5.
\end{align*}
$$
Since $X+2Y$ is a linear combination of normal variables, we have
$X+ 2Y \sim N(0,5)$ and thus
$$\mathbb{P}(X+2Y\leq 3)= \mathbb{P}\left( \frac{X+2Y}{\sqrt{ 5 }}\leq \frac{3}{\sqrt{ 5 }} \right)= \Phi\left( \frac{3}{\sqrt{ 5 }} \right).$$
##### Part 2

(...)
