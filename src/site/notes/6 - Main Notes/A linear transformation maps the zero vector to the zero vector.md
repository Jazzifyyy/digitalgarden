---
{"dg-publish":true,"permalink":"/6-main-notes/a-linear-transformation-maps-the-zero-vector-to-the-zero-vector/","tags":["linear_algebra","info"]}
---

### Statement

Suppose $U$ and $V$ are vector spaces and $T:U \rightarrow V$ is a [[6 - Main Notes/linear transformation\|linear transformation]]. Then we have
$$T(0_{U})=0_{V}.$$
### Proof
Take any $x \in U$. Then we have
$$\begin{align*}
T(0_{U}) &= T(x - x) \\
&= T(x) + T(-x) \\
&= T(x)- T(x) \\
&= 0_{V}.
\end{align*}$$