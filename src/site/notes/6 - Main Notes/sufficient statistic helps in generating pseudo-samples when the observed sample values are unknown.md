---
{"dg-publish":true,"permalink":"/6-main-notes/sufficient-statistic-helps-in-generating-pseudo-samples-when-the-observed-sample-values-are-unknown/","tags":["inference","info"]}
---

### Generation of samples given the value of a sufficient statistic

Suppose we have the model $(X_{1},\dots,X_{n})=\mathbf{X} \overset{\text{i.i.d}}{\sim} \mathcal{F}_{\theta}(\cdot)$ and consider the [[6 - Main Notes/sufficient statistic\|sufficient statistic]] $T(\cdot)$. Suppose we have an unknown observation $\mathbf{x}=(x_{1},\dots,x_{n})$, but the value $T(\mathbf{x})$ is known. 

We can generate a new sample $\mathbf{y}=(y_{1},\dots,y_{n})$ using the completely known conditional distribution:
$$\mathbb{P}_{t} \{ \mathbf{Y}=\mathbf{y} \}= \mathbb{P}_{\theta}\{ \mathbf{X}=\mathbf{y} \mid T(\mathbf{X})=t \}.$$
(This distribution is known since $T$ is sufficient.)

The generated sample $\mathbf{y}$ is such that $T(\mathbf{y})=t$.
### The unconditional distribution of $\mathbf{Y}$ is same as the unconditional distribution of $\mathbf{X}$

We have
$$\begin{align}
\mathbb{P}\{ \mathbf{Y}=\mathbf{y} \} &= \sum_{t \in T(\mathcal{X})}\mathbb{P}_{t}\{ \mathbf{Y}=y \}.\mathbb{P}_{\theta}\{ T(\mathbf{X})=t \} \\
&=\sum_{t \in T(\mathcal{X})} \mathbb{P}_{\theta}\{ \mathbf{X}=\mathbf{y} \mid T(\mathbf{X})=t \}. \mathbb{P}_{\theta}\{ T(\mathbf{X})=t \} \\
&= \mathbb{P}_{\theta}\{ \mathbf{X}=\mathbf{y} \}.
\end{align}$$
