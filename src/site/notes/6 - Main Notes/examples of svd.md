---
{"dg-publish":true,"permalink":"/6-main-notes/examples-of-svd/","tags":["linear_algebra","problem"]}
---

### Example

We wish to find the svd for
$$A = \begin{pmatrix}
3 & 5 \\
4 & 0
\end{pmatrix}.$$

We have
$$K = A^TA = \begin{pmatrix}
25 & 15 \\
15 & 25
\end{pmatrix}$$
and 
$$\begin{align}
\det(K - \lambda I) &= \det \begin{pmatrix}
25 - \lambda & 15 \\
15 & 25 - \lambda
\end{pmatrix} \\
&= (\lambda-10)(\lambda-40)
\end{align}$$
and thus the eigenvalues are $10$ and $40$ and
$$(K-10I)\mathbf{v}=0 \implies v_{1}+v_{2}=0$$
and
$$(K - 40I)\mathbf{v} = 0 \implies v_{1}=v_{2}.$$
Thus, the corresponding eigenvectors are $(1,-1)$ and $(1,1)$.

Set 
$$\mathbf{q}_{1}= \begin{pmatrix} \frac{1}{\sqrt{ 2 }}  \\
\frac{1}{\sqrt{ 2 }} \end{pmatrix}$$
and
$$\mathbf{q}_{2} = \begin{pmatrix}
-\frac{1}{\sqrt{ 2 }} \\
\frac{1}{\sqrt{ 2 }}
\end{pmatrix}$$

and construct $Q$ with these orthonormal vectors in its columns:
$$Q = \begin{pmatrix}
\frac{1}{\sqrt{ 2 }} & -\frac{1}{\sqrt{ 2 }} \\
\frac{1}{\sqrt{ 2 }} & \frac{1}{\sqrt{ 2 }}
\end{pmatrix}.$$
Next set $$\mathbf{p}_{1} = \frac{A\mathbf{q_{1}}}{\sigma_{1}}= \frac{1}{\sqrt{ 40 }} \begin{pmatrix}
4\sqrt{ 2 } \\
2 \sqrt{ 2 }
\end{pmatrix}=\begin{pmatrix}
\frac{2}{\sqrt{ 5 }} \\
\frac{1}{\sqrt{ 5 }}
\end{pmatrix}$$
and
$$\mathbf{p}_{2}= \frac{A\mathbf{q}_{2}}{\sigma_{2}}= \frac{1}{\sqrt{ 10 }}\begin{pmatrix}
\sqrt{ 2 } \\
-2\sqrt{ 2 }
\end{pmatrix}= \begin{pmatrix}
\frac{1}{\sqrt{ 5 }} \\
-\frac{2}{\sqrt{ 5 }}
\end{pmatrix}$$
and construct 
$$P = \begin{pmatrix}
\frac{2}{\sqrt{ 5 }} & \frac{1}{\sqrt{ 5 }} \\
\frac{1}{\sqrt{ 5 }} & -\frac{2}{\sqrt{ 5 }}
\end{pmatrix}.$$
Thus the svd decomposition is
$$\begin{pmatrix}
3 & 5 \\
4 & 0
\end{pmatrix} = \begin{pmatrix}
\frac{2}{\sqrt{ 5 }} & \frac{1}{\sqrt{ 5 }} \\
\frac{1}{\sqrt{ 5 }} & -\frac{2}{\sqrt{ 5 }}
\end{pmatrix} \begin{pmatrix}
\sqrt{ 40 } & 0 \\
0 & \sqrt{ 10 }
\end{pmatrix}\begin{pmatrix}
\frac{1}{\sqrt{ 2 }} & \frac{1}{\sqrt{ 2 }} \\
-\frac{1}{\sqrt{ 2 }} & \frac{1}{\sqrt{ 2 }}
\end{pmatrix}.$$




