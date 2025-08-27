---
{"dg-publish":true,"permalink":"/6-main-notes/multivariate-normal-distribution/","tags":["probability_theory","info"]}
---

### Definition

The random vector $(X_{1},\dots,X_{d})$ is said to have a **multivariate normal distribution** iff its joint density is given by
$$f_{\mathbf{X}}(\mathbf{x})= \frac{1}{(2\pi)^{d/2}\sqrt{ \det \Sigma }}\exp\left\{  -\frac{1}{2}(\mathbf{x} - \bar{\mu})^T \Sigma^{-1}(\mathbf{x}-\bar{\mu}) \right\}$$
where $\Sigma$ is the [[6 - Main Notes/variance-covariance matrix\|variance-covariance matrix]].

### Notation

Write this as 
$$\mathbf{X} \sim \mathcal{N}_{d}(\bar{\mu}, \Sigma).$$
