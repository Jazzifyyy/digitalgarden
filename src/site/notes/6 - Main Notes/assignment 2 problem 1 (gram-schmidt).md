---
{"dg-publish":true,"permalink":"/6-main-notes/assignment-2-problem-1-gram-schmidt/","tags":["linear_algebra","info"]}
---

### Problem

Find an orthonormal basis of 
$$P_{3}:= \{ f \mid \deg f < 3\}$$
with respect to the inner product 
$$\langle f, g \rangle := \int_{0}^1 f(t)g(t)dt.$$
### Solution

We know that $(\mathbf{w}_{1}, \mathbf{w}_{2}, \mathbf{w}_{3})=(1, x, x^2)$ is a basis for $P_{3}$.

Set $\mathbf{\mathbf{v}_{1}}=\mathbf{w}_{1}=1$.

Set
$$\begin{align}
\mathbf{v}_{2} &=\mathbf{w}_{2} - \frac{\langle \mathbf{w}_{2}, \mathbf{v}_{1} \rangle}{\Vert\mathbf{v}_{1} \Vert^2}\mathbf{v}_{1} \\
&= x - \frac{\int_{0}^1 tdt}{\int_{0}^1 dt} \\
&= x - \frac{1}{2}.
\end{align}$$
Set
$$\begin{align}
\mathbf{v}_{3} &=\mathbf{w}_{3}-\frac{\langle \mathbf{w}_{3}, \mathbf{v}_{1} \rangle}{\Vert \mathbf{v}_{1} \Vert^2}\mathbf{v}_{1}-\frac{\langle \mathbf{w}_{3}, \mathbf{v}_{2} \rangle}{\Vert \mathbf{v}_{2} \Vert^2} \mathbf{v}_{2} \\
&= x^2 - \frac{\int_{0}^1 t^2dt}{\int_{0}^1 dt}- \frac{\int_{0}^1 t^2\left( t - \frac{1}{2} \right)dt}{\int_{0}^1 \left( t - \frac{1}{2} \right)^2 dt}\left( x - \frac{1}{2} \right) \\
&= x^2 - \frac{1}{3} - \frac{\left[ \frac{t^4}{4}-\frac{1}{6}t^3 \right]^{1}_{0}}{\left[ \frac{t^3}{3}+ \frac{t}{4} - \frac{t^2}{2} \right]^1_{0}}\left( x - \frac{1}{2} \right) \\
&= x^2 - \frac{1}{3} - \frac{\frac{1}{12}}{\frac{1}{12}}\left( x - \frac{1}{2} \right) \\
&= x^2 - \frac{1}{3} - x + \frac{1}{2} \\
&= x^2 -x + \frac{1}{6}.
\end{align}$$

We have $\Vert \mathbf{v}_{1} \Vert^2 = 1$ and $\Vert \mathbf{v}_{2} \Vert^2 = \frac{1}{12}$ from previous calculations and
$$\begin{align}
\Vert \mathbf{v}_{3} \Vert^2 &= \int_{0}^1 \left( t^2 - t + \frac{1}{6} \right)^2 dt \\
&= \int_{0}^1 \left(t^4 +t^2 + \frac{1}{36}-2t^3 +\frac{t^2}{3} -\frac{t}{3}\right)dt \\
&= \left(\frac{t^5}{5}+ \frac{t^3}{3} + \frac{t}{36} - \frac{t^4}{2} + \frac{t^3}{9} - \frac{t^2}{6}\right)_{0}^1 \\
&= \frac{1}{180}.
\end{align}$$
Thus the orthogonal vectors are 
$$(\mathbf{e}_{1}, \mathbf{e}_{2}, \mathbf{e}_{3})= \left( 1, 2\sqrt{ 3 }\left( x - \frac{1}{2} \right), 6\sqrt{ 5 }\left( x^2 - x + \frac{1}{6} \right) \right).$$
