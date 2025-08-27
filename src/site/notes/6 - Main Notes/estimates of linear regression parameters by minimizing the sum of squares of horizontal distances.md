---
{"dg-publish":true,"permalink":"/6-main-notes/estimates-of-linear-regression-parameters-by-minimizing-the-sum-of-squares-of-horizontal-distances/","tags":["regression","info"]}
---

We can estimate the parameters of a [[6 - Main Notes/linear regression model\|linear regression model]] by minimizing the sum of squares of horizontal distances of the data points from the line. 

Rewrite the linear regression model as
$$x_{i}=\alpha_{0}+\alpha_{1}y_{i} + \varepsilon_{i}$$
for $i \in \{ 1,\dots,n \}$.

$$\underset{{\alpha_{0}}, {\alpha_{1}}}{\text{argmin}} \sum_{i=1}^n (x_{i}-\alpha_{0}-\alpha_{1}y_{i})^2= (\hat{\alpha}_{0}, \hat{\alpha}_{1})$$
yielding
$$\hat{\alpha}_{1}= \frac{\sum_{i=1}^n(x_{i}- \bar{x})(y_{i} - \bar{y})}{\sum_{i=1}^n (y_{i}- \bar{y})^2}$$
and
$$\hat{\alpha}_{0}= \bar{x}-\hat{\alpha}_{1}\bar{y}.$$
### Also See:
+ [[6 - Main Notes/the product of the estimates of the slopes from the horizontal distance minimizer and the vertical distance minimizer is equal to the sample correlation coefficient (linear regression)\|the product of the estimates of the slopes from the horizontal distance minimizer and the vertical distance minimizer is equal to the sample correlation coefficient (linear regression)]]