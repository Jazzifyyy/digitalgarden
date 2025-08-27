---
{"dg-publish":true,"permalink":"/6-main-notes/why-regression-and-how-to-do-it-in-practice/","tags":["regression","info"]}
---

### Some uses of regression
+ To *predict* $y$ given some new $x_{1},\dots,x_{p}$.
+ To study the *impact* of a predictor on the response. For instance, one can ask "what is the change in response for a unit change in the predictor?".
+ Hypothesis testing. For example, keeping "education" and "experience" fixed, does gender effect "salary"?
### In practice

We usually start with a scatterplot and ensure that a linear model is reasonable (visually).

The following steps are repeated until we have a model that satisfied all assumptions.
#### Fitting
+ Estimate the parameters $(\beta_{0},\beta_{1}, \sigma^2)$. (See: [[6 - Main Notes/linear regression model\|linear regression model]])
#### Diagnostics
+ Verify if the model assumptions are satisfied. 
#### Modification
+ If the model assumptions are not satisfied, modify the model and go back to step 1. 
