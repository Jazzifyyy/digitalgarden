---
{"dg-publish":true,"permalink":"/6-main-notes/gram-schmidt-process/","tags":["linear_algebra","info"]}
---

### Goal

Let $W$ denote a finite-dimensional [[6 - Main Notes/inner product space\|inner product space]]. We assume that we already know some basis $\{ \mathbf{w}_{1},\dots, \mathbf{w}_{n} \}$ of $W$, where $n =\dim W$. 

Our goal is to use this information to construct an orthogonal basis $\mathbf{v}_{1},\dots,\mathbf{v}_{n}$.

### Process

+ Set $\mathbf{v}_{1}:=\mathbf{w}_{1}$. (Note that $\mathbf{v}_{1} \neq 0$, since $\mathbf{w}_{1}$ appears in the original basis.)
+ Set 
  $$\mathbf{v}_{2}:=\mathbf{w}_{2} - \frac{\langle \mathbf{w}_{2}, \mathbf{v}_{1} \rangle}{\Vert\mathbf{v}_{1} \Vert^2}\mathbf{v}_{1}.$$
  We get this in an attempt to find $c$ such that $\mathbf{v}_{2}=\mathbf{w}_{2} - c \mathbf{v}_{1}$ is orthogonal to $\mathbf{v}_{1}$, thus, the equation
  $$0 = \langle \mathbf{v_{2}}, \mathbf{v}_{1} \rangle = \langle \mathbf{w}_{2}, \mathbf{v}_{1} \rangle - c \langle\mathbf{v}_{1}, \mathbf{v}_{1}\rangle=\langle \mathbf{w}_{2}, \mathbf{v}_{1} \rangle - c \Vert \mathbf{v}_{1} \Vert^2$$
  yields the required $c$.
  
  Also note that the linear independence of $\mathbf{w}_{2}$ and $\mathbf{w}_{1}$ ensures that $\mathbf{v}_{2} \neq 0$.
+ Set
  $$\mathbf{v}_{3}:=\mathbf{w}_{3}-\frac{\langle \mathbf{w}_{3}, \mathbf{v}_{1} \rangle}{\Vert \mathbf{v}_{1} \Vert^2}\mathbf{v}_{1}-\frac{\langle \mathbf{w}_{3}, \mathbf{v}_{2} \rangle}{\Vert \mathbf{v}_{2} \Vert^2} \mathbf{v}_{2}.$$
  Once again, we get this in an attempt to find $c_{1}$ and $c_{2}$ such that $\mathbf{v}_{3}=\mathbf{w}_{3}-c_{1}\mathbf{v}_{1}-c_{2}\mathbf{v}_{2}$ is orthogonal to both $\mathbf{v}_{1}$ and $\mathbf{v}_{2}$, thus the equations (note that $\langle \mathbf{v_{1}}, \mathbf{v}_{2} \rangle = 0$)  
  $$0 = \langle \mathbf{v_{3}}, \mathbf{v}_{1} \rangle = \langle \mathbf{w}_{3}, \mathbf{v}_{1} \rangle - c_{1} \langle\mathbf{v}_{1}, \mathbf{v}_{1}\rangle=\langle \mathbf{w}_{3}, \mathbf{v}_{1} \rangle - c_{1} \Vert \mathbf{v}_{1} \Vert^2$$
  and
  $$0 = \langle \mathbf{v_{3}}, \mathbf{v}_{2} \rangle = \langle \mathbf{w}_{3}, \mathbf{v}_{1} \rangle - c_{2} \langle\mathbf{v}_{2}, \mathbf{v}_{2}\rangle=\langle \mathbf{w}_{3}, \mathbf{v}_{1} \rangle - c_{2} \Vert \mathbf{v}_{2} \Vert^2.$$
  yield the required $c_{1}$ and $c_{2}$.
  
  ### Problems
+ [[6 - Main Notes/assignment 2 problem 1 (gram-schmidt)\|assignment 2 problem 1 (gram-schmidt)]]
