---
{"dg-publish":true,"permalink":"/6-main-notes/big-o-notation/","tags":["dsa","info"]}
---

### Definition

Given two functions $f$ and $g$, we say that $f \in O(g)$ if there exists constants $c>0$ and $n_{0}>0$ such that 
$$f(n) \leq cg(n)$$
for all $n \geq n_{0}$.

### Note

Note that the big-o notation makes a weaker statement than the corresponding [[6 - Main Notes/Little-o notation\|little-o notation]].

### Insight

Big-o notation is useful for analyzing the efficiency of algorithms. For instance, the time/steps required to complete a problem of size $n$ might be $T(n)= 4n^2 - 2n+2$.

Observe the following points:

1. Note that as $n$ grows large, the $n^2$ term will dominate the other terms - for example, for $n=500$, the term $4n^2$ is $1000$ times larger than the $2n$ term. 
2. Further, the coefficients starts becoming irrelevant if we compare $T$ to any other expression of a different order - for example, if $T(n)=10000n^2$ and $U(n)= n^3$, the latter will always exceed the former once $n$ grows larger than $10000$ (since $T(10000)=U(10000)=10000^3$).
3. Additionally, the number of steps also depends on the machine on which the algorithm runs. Usually, the number of steps required to execute an algorithm on different machines vary by only a constant factor.  

The big-o notation essentially tries to ignore all these points and only record the essential question - "How quickly does the algorithm *grow*?". Now we may write $f(n) \in O(n^2)$ and say that "the algorithm has *order of $n^2$* time complexity".

### Properties

1. If a function $f$ can be written as the finite sum of other functions, then the fastest growing one determines the order of $f$. For example, 
$$f(n)=9\log n+ 5(\log n)^4+ 2n^3 \in O(n^3).$$
2. Any powers of $n$ inside the logarithms is ignored by big-o notation, i.e., $O(\log n)= O(\log n^c)$. The logarithms only differ by a constant factor since $\log n^c=c\log n$ and thus the big-o notation ignores that.
3. Similarly, logarithms with different constant bases are equivalent, i.e., $O(\log_{a}n)=O(\log_{b}n)$ because $\log_{a}n= \frac{1}{\log_{b}a}\log_{b}n$.
4. Exponentials of different bases are NOT of the same order, for example, $2^n$ and $3^n$ are not of the same order. 
5. Changing units may or may not affect the order of the algorithm.
6. Change in variable may affect the order of the algorithm. 