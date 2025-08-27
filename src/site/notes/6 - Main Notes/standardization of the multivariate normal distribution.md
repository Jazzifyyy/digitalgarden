---
{"dg-publish":true,"permalink":"/6-main-notes/standardization-of-the-multivariate-normal-distribution/","tags":["probability_theory","info"]}
---

(See: [[6 - Main Notes/Multivariate normal distribution\|Multivariate normal distribution]])
### Statement

Suppose $(X_{1},\dots,X_{d})=\mathbf{X} \sim \mathcal{N}_{d}(\bar{\mu}_{d},\Sigma_{d\times d})$ and suppose $\Sigma=LL^T$ is the Cholesky decomposition of $\Sigma$. 

Then 
$$\mathbf{Z}=L^{-1}(\mathbf{X}-\bar{\mu}) \sim \mathcal{N}_{2}(0, I_{d}).$$

