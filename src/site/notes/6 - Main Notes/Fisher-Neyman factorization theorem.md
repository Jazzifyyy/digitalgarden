---
{"dg-publish":true,"permalink":"/6-main-notes/fisher-neyman-factorization-theorem/","tags":["inference","info"]}
---

### Statement

Suppose $p_{\theta}(\mathbf{x})$ is the joint pdf/pmf of the sample $\mathbf{X}$. A [[6 - Main Notes/Statistic (inference fall)\|statistic]] $T(\mathbf{X})$ is a [[6 - Main Notes/Sufficient statistic\|sufficient statistic]] for $\theta$ iff we can factorize $p_{\theta}(\mathbf{x})$ as
$$p_{\theta}(\mathbf{x})= g_{\theta}[T(\mathbf{x})]h(\mathbf{x})$$
for all $\mathbf{x} \in \mathcal{X}$, where $g_{\theta}[T(\cdot)]$ is a function that depends on $\theta$ and $T(\cdot)$ and $h(\cdot)$ is a function free of $\theta$. 
### Proof

##### If part

Suppose we have $p_{\theta}(\mathbf{x})= g_{\theta}[T(\mathbf{x})]h(\mathbf{x})$. 

If $T(\mathbf{x}) \neq t$. Then $\mathbb{P}_{\theta}\{ \mathbf{X}=\mathbf{x} | T(\mathbf{X})=t \}=0$ and is thus free of $\theta$.

If $T(\mathbf{x})=t$, then
$$\begin{align}
\mathbb{P}_{\theta}\{ \mathbf{X}=\mathbf{x} | T(\mathbf{X})=t \} &= \frac{p_{\theta}(\mathbf{x})}{\mathbb{P}_{\theta}\{ T(\mathbf{X})=t \}} \\
&= \frac{p_{\theta}(\mathbf{x})}{\sum_{\mathbf{y} \in A_{t}}p_{\theta}(\mathbf{y})} \\
(\text{Note that } A_{t}=A_{T(\mathbf{x})})
&= \frac{p_{\theta}(\mathbf{x})}{\sum_{\mathbf{y} \in A_{T(\mathbf{x})}}g_{\theta}[T(\mathbf{y})]h(\mathbf{y})} \\
&= \frac{g_{\theta}[T(\mathbf{x})]h(\mathbf{x})}{\sum_{\mathbf{y} \in A_{T(\mathbf{x})}}g_{\theta}[T(\mathbf{x})]h(\mathbf{y})} \\
&= \frac{h(\mathbf{x})}{\sum_{\mathbf{y} \in A_{T(\mathbf{x})}}h(\mathbf{y})} \\
\end{align}$$
which is free of $\theta$. 

Therefore, $T(\mathbf{X})$ is sufficient for $\theta$.
##### Only if part

Suppose that $T(\mathbf{X})$ is sufficient of $\theta$.

Note
$$\begin{align}
p_{\theta}(\mathbf{x}) &= \mathbb{P}_{\theta}\{ \mathbf{X}= \mathbf{x}\} \\
&= \sum_{t \in T(\mathcal{X})}\mathbb{P}_{\theta}\{ \mathbf{X}=\mathbf{x}| T(\mathbf{X})=t \}.\mathbb{P}_{\theta}\{ T(\mathbf{X}) =t\} \\
&= \mathbb{P}_{\theta}\{ T(\mathbf{X})=T(\mathbf{x}) \} \cdot\sum_{t | t = T(\mathbf{x})}\mathbb{P}_{\theta}\{ \mathbf{X}=\mathbf{x} |T(\mathbf{X})=t \} \\
&= \mathbb{P}_{\theta}\{ T(\mathbf{X})=T(\mathbf{x}) \}. \mathbb{P_{\theta}}\{ \mathbf{X}=\mathbf{x} | T(\mathbf{X})=T(\mathbf{x})\} 
\end{align}$$
Set $g_{\theta}[T(\cdot)]:= \mathbb{P_{\theta}}\{ T(\mathbf{.})=T(\mathbf{.}) \}$ and $h(\cdot):= \mathbb{P}_{\theta}\{ \mathbf{X}=\cdot|T(\mathbf{X})=T(\cdot) \}$ and we are done. 

