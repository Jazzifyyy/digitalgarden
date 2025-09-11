---
{"dg-publish":true,"permalink":"/6-main-notes/examples-of-linear-transformation/","tags":["linear_algebra","problem"]}
---

### Example 1

For the vector space $\mathbb{R}^2$ over $\mathbb{R}$, define the function $T:\mathbb{R}^2 \rightarrow \mathbb{R}^2$ by $T(x_{1},x_{2})=(x_{1},-x_{2})$. Then $T$ is a linear transformation.

Geometrically, such a $T$ denotes a reflection about the $x$-axis. 
##### Proof

For any $x=(x_{1},x_{2})$ and $y=(y_{1},y_{2})$ in $\mathbb{R}^2$, we have
$$\begin{align*}
T(x+y) &= T(x_{1}+y_{1}, x_{2} + y_{2}) \\
&= (x_{1}+y_{1}, -x_{2}-y_{2})\\
&= (x_{1}, -x_{2})+ (y_{1},-y_{2}) \\
&= T(x)+ T(y).
\end{align*}$$
Further for any $\alpha \in \mathbb{R}$,
$$\begin{align*}
T(\alpha x) &= T(\alpha x_{1}, \alpha x_{2}) \\
&= (\alpha x_{1}, -\alpha x_{2})\\
&= \alpha(x_{1},-x_{2}) \\
&= \alpha T(x).
\end{align*}$$
### Example 2

For the vector space $\mathbb{R}^3$ over $\mathbb{R}$, define the function $T:\mathbb{R}^3 \rightarrow \mathbb{R}^3$ by $T(x_{1},x_{2},x_{3})=(x_{1},x_{2},0)$. Then $T$ is a linear transformation.

Geometrically, such a $T$ denotes an orthogonal projection on the $xy$ plane.

##### Proof

For any $x=(x_{1},x_{2},x_{3})$ and $y=(y_{1},y_{2},y_{3})$ in $\mathbb{R}^3$, we have
$$\begin{align*}
T(x+y) &= T(x_{1}+y_{1}, x_{2} + y_{2}, x_{3}+y_{3}) \\
&= (x_{1}+y_{1}, x_{2}+y_{2},0)\\
&= (x_{1}, x_{2}, 0)+ (y_{1},y_{2},0) \\
&= T(x)+ T(y).
\end{align*}$$
Further for any $\alpha \in \mathbb{R}$,
$$\begin{align*}
T(\alpha x) &= T(\alpha x_{1}, \alpha x_{2}, \alpha x_{3}) \\
&= (\alpha x_{1}, \alpha x_{2},0)\\
&= \alpha(x_{1},x_{2},0) \\
&= \alpha T(x).
\end{align*}$$
### Example 3

For the vector space $\mathbb{R}^2$ over $\mathbb{R}$, define the function $T:\mathbb{R}^2 \rightarrow \mathbb{R}^2$ by $T(x_{1},x_{2})=(x_{1}+1,x_{2})$. Then $T$ is NOT a linear transformation.

##### Proof

Note that we have $T(0,0)=(1,0)$ which is a contradiction to [[6 - Main Notes/A linear transformation maps the zero vector to the zero vector\|A linear transformation maps the zero vector to the zero vector]].

### Example 4

For the vector space $\mathbb{M}_{2}(\mathbb{C})$ (the set of all $2 \times 2$ matrices over $\mathbb{C}$), define the function $T: \mathbb{M}_{2}(\mathbb{C}) \rightarrow \mathbb{C}$ by $T(A)= \mathrm{Tr}(A)$. 

Then $T$ is a linear transformation by the properties of trace.

### Example 5

For the vector space $\mathbb{M}_{2}(\mathbb{C})$ (the set of all $2 \times 2$ matrices over $\mathbb{C}$), define the function $T: \mathbb{M}_{2}(\mathbb{C}) \rightarrow \mathbb{M}_{2}(\mathbb{C})$ by $T(A)= A^T$.

Then $T$ is a linear transformation by the properties of transpose.