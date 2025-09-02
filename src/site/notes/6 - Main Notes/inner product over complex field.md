---
{"dg-publish":true,"permalink":"/6-main-notes/inner-product-over-complex-field/","tags":["linear_algebra","info"]}
---

### Definition

Suppose $X$ is a vector space over the complex field. An **inner product** on $X$ is a function $\langle .,. \rangle: X \times X \rightarrow \mathbb{C}$ such that, for all $x,y,z, \in X$ and $\alpha,\beta \in \mathbb{C}$, we have
1. $\langle x, x \rangle \in \mathbb{R}$, $\langle x, x \rangle \geq0$ and $\langle x,x\rangle=0 \iff x=0$.
2. $\langle \alpha x+\beta y, z\rangle=\alpha \langle x,z \rangle+ \beta \langle y,z \rangle$.
3. $\langle x,y \rangle = \overline{\langle y,x \rangle}$.
### Examples

##### Example 1

The map $\langle .,. \rangle:\mathbb{C}^k\times \mathbb{C}^k \rightarrow \mathbb{C}$ defined by 
$$\langle x,y \rangle = \sum_{n=1}^k x_{n} \bar{y}_{n}$$
is an inner product on $\mathbb{C}^k$.