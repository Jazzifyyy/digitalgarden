---
{"dg-publish":true,"permalink":"/6-main-notes/inverse-image-under-a-statistic/","tags":["inference","info"]}
---

### Definition

Suppose we have a [[6 - Main Notes/Statistic (inference fall)\|statistic]] $T: \mathcal{X}\rightarrow T(\mathcal{X})$. Then for any $t \in T(\mathcal{X})$, define
$$A_{t} := \{ \mathbf{x} \in \mathcal{X} \mid T(\mathbf{x})=t \}.$$
### Partitioning of the sample space 

The sample space $\mathcal{X}$ is partitioned by the sets $A_{t}$ where $t \in T(\mathcal{X})$.
##### Property 1

For all $\mathbf{x} \in \mathcal{X}$, there exists some $t \in T(\mathcal{X})$ such that $\mathbf{x} \in A_{t}$.

(Trivially, we have $\mathbf{x} \in A_{T(\mathbf{x})}$.)
##### Property 2

Every $\mathbf{x} \in \mathcal{X}$ can belong to exactly one $A_{t}$.

(Suppose $\mathbf{x} \in A_{t_{1}}$ and $\mathbf{x} \in A_{t_{2}}$. Then $T(\mathbf{x})=t_{1}$ and also $T(\mathbf{x})=t_{2}$, but since $T$ is a function, we have $t_{1}=t_{2}$.)