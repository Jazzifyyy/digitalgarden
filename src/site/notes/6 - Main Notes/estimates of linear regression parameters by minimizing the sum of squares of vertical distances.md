---
{"dg-publish":true,"permalink":"/6-main-notes/estimates-of-linear-regression-parameters-by-minimizing-the-sum-of-squares-of-vertical-distances/","tags":["regression","info"]}
---

We can estimate the parameters of a [[6 - Main Notes/linear regression model\|linear regression model]] by minimizing the sum of squares of vertical distances of the data points from the line. 
$$\underset{{\beta_{0}}, {\beta_{1}}}{\text{argmin}} \sum_{i=1}^n (y_{i}-\beta_{0}-\beta_{1}x_{i})^2= (\hat{\beta_{0}}, \hat{\beta_{1}})$$
yielding

$$\hat{\beta_{1}}= \frac{\sum_{i=1}^n(x_{i}- \bar{x})(y_{i} - \bar{y})}{\sum_{i=1}^n (x_{i}- \bar{x})^2}$$
and
$$\hat{\beta_{1}}= \bar{y} - \hat{\beta_{1}}\bar{x}.$$

### Also See:
+ [[6 - Main Notes/alternative expressions for the linear regression line\|alternative expressions for the linear regression line]]
+ [[6 - Main Notes/the product of the estimates of the slopes from the horizontal distance minimizer and the vertical distance minimizer is equal to the sample correlation coefficient (linear regression)\|the product of the estimates of the slopes from the horizontal distance minimizer and the vertical distance minimizer is equal to the sample correlation coefficient (linear regression)]]