---
{"dg-publish":true,"permalink":"/6-main-notes/set-4-ex-2-extreme-order-statistics-of-uniform-distribution/","tags":["inference","problem"]}
---

### Problem

Suppose $X_{1},\dots,X_{n} \overset{\text{i.i.d}}{\sim} \text{Uniform}(0, \theta)$, where $\theta>0.$

1. Determine $\mathbb{E}[X_{(1)}]$ and $\mathbb{E}[X_{(n)}]$.
2. Define $R_{n}=X_{(n)}- X_{(1)}$ to be the range of the sample $X_{1},\dots,X_{n}$. Find $\mathbb{E}[R_{n}]$.
3. What can you say about $R_{n}$ as $n \rightarrow \infty$?

### Solution

##### Part 1

Recall: [[6 - Main Notes/distribution of the jth order statistic\|distribution of the jth order statistic]].

Note that $F_{X}(x)=\int_{0}^x \frac{1}{\theta}dt=\frac{x}{\theta}$ for $x \in (0, \theta]$.

For $0<y< \theta$, we have 
$$
\begin{align}
f_{(1)}(y) &= \frac{n!}{(1-1)!(n-1)!}\left( \frac{y}{\theta} \right)^{1-1}\left( 1- \frac{y}{\theta} \right)^{n-1}\left( \frac{1}{\theta} \right) \\
&= \frac{n}{\theta}\left( 1 - \frac{y}{\theta} \right)^{n-1}
\end{align}$$
and
$$
\begin{align}
f_{(n)}(y) &= \frac{n!}{(n-1)!(n-n)!}\left( \frac{y}{\theta} \right)^{n-1}\left( 1 - \frac{y}{\theta} \right)^{n-n}\left( \frac{1}{\theta} \right) \\
&= \frac{n}{\theta}\left( \frac{y}{\theta} \right)^{n-1}.
\end{align}$$
Now
$$\begin{align}
\mathbb{E}[X_{(1)}]&=\int_{-\infty}^\infty y f_{(1)}(y)dy \\
&= \int_{0}^\theta y \left( \frac{n}{\theta} \right)\left( 1 - \frac{y}{\theta} \right)^{n-1}dy.
\end{align}$$
Set $t= 1 - \frac{y}{\theta}$, with $dt = -\frac{dy}{\theta}$.
$$\begin{align}
&= \int_{0}^1 n\theta(1-t)(t)^{n-1}dt \\
&= n\theta\left[ \frac{t^n}{n}-\frac{t^{n+1}}{n+1} \right]^{1}_{0} \\
&= n\theta \left( \frac{1}{n(n+1)} \right) \\
&= \frac{\theta}{n+1}
\end{align}$$
and
$$\begin{align}
\mathbb{E}[X_{(n)}] &= \int_{-\infty}^\infty yf_{(n)}(y)dy \\
&= \int_{0}^\theta y \left( \frac{n}{\theta} \right)\left( \frac{y}{\theta} \right)^{n-1}dy \\
&= \frac{n}{\theta^{n}}\int_{0}^\theta y^n dy \\
&= \frac{n}{\theta^{n}} \left( \frac{\theta^{n+1}}{n+1} \right)  \\
&= \frac{n\theta}{n+1}.
\end{align}$$
##### Part 2

We have
$$\begin{align}
\mathbb{E}[R_{n}] &= \mathbb{E}[X_{(n)}- X_{(1)}] \\
&= \mathbb{E}[X_{(n)}]- \mathbb{E}[X_{(1)}] \\
&= \frac{n}{n+1}\theta - \frac{1}{n+1}\theta \\
&= \frac{n-1}{n+1}\theta.
\end{align}$$
##### Part 3

We have $\mathbb{E}[R_{n}] \rightarrow \theta$ as $n \rightarrow \infty$. 

Therefore, for large samples, the sample range $R_{n}= X_{(n)}-X_{(1)}$ gets close to the population range $\theta-0=\theta$.