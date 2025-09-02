---
{"dg-publish":true,"permalink":"/6-main-notes/assignment-2-problem-4-conditional-distribution-and-bivariate-normal/","tags":["probability_theory","info"]}
---

### Problem

Suppose that $W \sim \mathcal{N}(\mu, \sigma^2)$ and suppose that $Z |W=w \sim \mathcal{N}(aw+b, \tau^2)$. 
1. Show that the joint distribution of $W$ and $Z$ is bivariate normal. Find its parameters.
2. What is the marginal distribution of $Z$?
3. What is the conditional distribution of $W$ given $Z=z$?

### Solution

$$\begin{align}
f_{Z,W}(z,w) &= f_{Z|W=w}(z|w).f_{W}(w) \\
&= \frac{1}{\tau \sqrt{ 2\pi }}\exp\left\{  -\frac{1}{2}\left(\frac{z-aw-b}{\tau}\right)^2  \right\}. \frac{1}{\sqrt{ 2\pi }}\exp\left\{  -\frac{1}{2}\left( \frac{w-\mu}{\sigma} \right)^2  \right\} \\
&= \frac{1}{2\pi \tau}\exp \left\{  -\frac{1}{2}\left[ \frac{(x-b)^2+a^2w^2-2aw(x-b)}{\tau^2} + \frac{}{} \right]  \right\}
\end{align}$$



