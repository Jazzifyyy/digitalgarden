---
{"dg-publish":true,"permalink":"/6-main-notes/gram-matrix/","tags":["linear_algebra","info"]}
---

### Definition

Suppose $(V,\langle .,. \rangle)$ is a real [[6 - Main Notes/inner product space\|inner product space]] and suppose $\beta = \{ b_{1},\dots,b_{n} \}$ is a basis for $V$. Then $G$ defined by $g_{ij}=\langle b_{i}, b_{j} \rangle$ is called the **gram matrix** associated with that inner product space.

### Corollary

For any $x,y \in V$, 
$$\langle x,y \rangle =yG x^T$$
where $y = y_{\beta}=(y_{1},\dots, y_{n})$ and $x=x_{\beta}=(x_{1},\dots,x_{n})$.

##### Proof

We can express the inner product in the following way:
$$\begin{align}
\langle x,y \rangle &= \langle x_{1}b_{1}+\dots+x_{n}b_{n}, y_{1}b_{1}+\dots y_{n}b_{n} \rangle \\
&= y_{1}\langle b_{1},b_{1} \rangle x_{1}+ y_{1}\langle b_{2},b_{1}\rangle x_{2}+\dots \\
&+ y_{2}\langle b_{1}, b_{2}\rangle x_{1}+ y_{2} \langle b_{2},b_{2}\rangle x_{2}+\dots \\
& \cdot \\
&\cdot \\
&+y_{n} \langle b_{1}, b_{n}\rangle x_{1}+ y_{n} \langle b_{2},b_{n}\rangle x_{2}+\dots \\
&= (y_{1},y_{2},\dots,y_{n}) \begin{pmatrix}
\langle b_{1},b_{1}\rangle & \langle b_{2},b_{1} \rangle &\dots &\langle b_{n},b_{1} \rangle \\
\langle b_{1},b_{2} \rangle &\dots & &. \\
. & & &. \\
. & & & . \\
\langle b_{1},b_{n} \rangle & \dots & & \langle b_{n},b_{n} \rangle
\end{pmatrix}
\begin{pmatrix}
x_{1} \\
x_{2} \\
. \\
. \\
x_{n}
\end{pmatrix}.
\end{align}$$


