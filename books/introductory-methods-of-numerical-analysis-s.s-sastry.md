---
title: 'Introductory Methods of Numerical Analysis'
description: 'A book on Introductory Methods of Numerical Analysis for higher mathematics.'
author: ['S.S Sastry']
tags: ['maths', 'math', 'mathematics', 'numerical analysis', 'numerical methods', 'analysis']
---

# Introductory Methods of Numerical Analysis

## 1. Errors in Numerical Calculations

### 1.1 Introduction

`transcendental equations` : Simply functions that are not algebraic, i.e. it can not be expressed as a finite combination of the basic algebraic operations (add, sub, mul, div, taking roots etc)
For ex:

- $e^x$

- $logx$

- $sin^{-1}x$

These functions are typically not solved with algebraic operations but require numerical methods.

##### The book deals with areas of maths including:

- Algebraic and Transcendental Eq of type f(x) = 0, where f(x) is some function.

- **Interpolation** : if the explicit nature of a function say f(x) is not known, it is often required to find approximations for the function so as to find some `y` for some `x` where x is ranging between the known values of inputs for the function.

- **Curve Fitting** : a way to find approximations where there are high chances of error in the data points.
  The solution is to fit a curve which passes through the data points.

- **Numerical differentiation and Integration** : Yet to learn anything about this.

- **Matrices and Linear Systems**

- **ODE and PDE**

- **Integral Equations**

### 1.2 Mathematical Preliminaries

<u>**Theorem 1.1**</u>: if f(x) is continuous in a<=x<=b and if f(a) and f(b) are of opposite signs, then there must exist f(alpha) = 0 where a < alpha < b.

**<u>Theorem 1.2</u>** : (Rolle's Theorem) If f (x) is continuous in a<=x<=b, f '(x) exists in a < x < b and f (a) = f (b) = 0, then, there exists at least one value of x, say alpha such that f' (alpha) = 0, a < alpha < b.
Visually, this means there's a point 'c' where the tangent line to the graph of f(x) is horizontal.

<u>**Theorem 1.3**</u> : (Generalized Rolle's Theorem) If a function is n times differentiable on [a,b], if that function vanishes at (n+1) distinct points, x<sub>0</sub>, x<sub>1</sub>, . . . , x<sub>n</sub>, in (a,b) there exists a number alpha in (a,b) such that the f<sup>n</sup>(alpha) = 0.
*Simply: The Generalized Rolle's Theorem says that if a function has n distinct roots (places where the function equals zero) within an interval, then there must be a point within that interval where the nth derivative is zero.*

<u>**Theorem 1.4**</u> : (Intermediate value theorem) Let f (x) be continuous in [a, b] and let k be any number between f (a) and f (b). Then there exists a number alpha in (a, b) such that f(alpha) = k 

<u>**Theorem 1.5**</u> : Mean Value Theorem for derivatives.

<u>**Theorem 1.6**</u> : (Taylor's series for a function of one variable)
$f(x) = f(a) + (x-a)f'(a) + \frac{(x-a)^2}{2!}f''(a) + ... + \frac{(x-a)^{n-1}}{(n-1)!}f^{n-1}(a) + R_n(x)$

where R<sub>n</sub>(x), the remainder term can be expressed in the form 

$R_n(x) = \frac{(x-a)^{n-1}}{(n-1)!}f^n(\alpha), a<\alpha<x$

**<u>Theorem 1.7</u>** : Maclaurin's expansion

**<u>Theorem 1.8</u>** (Taylor's series for a function of two variables)

**<u>Theorem 1.9</u>** : (Taylor's series for a function of several variables)

### 1.3 Errors and their Computations

- Two types of numbers: <u>exact</u> and <u>approximate</u>
- Concept of significant digits.
- Concept of absolute, relative and percentage errors.

### 1.4 A General Error Forumla

- Formulating error in a given function.

### 1.5 Error in a series approximation

- Concept of resolving the truncated error in a seires approximation can be evaluated by using Taylor's series [Theorem 1.6](#mathematical-preliminaries)
- For convergent series the last term ( remainder term ) tends to 0 for a convergent series.

---

## Interpolation

### 3.1 Introduction

Interpolation involves estimating the value of a function at a point within the range of known data points.

**<u>Significance</u>** : Interpolation has a long history rooted in astronomy. Early astronomers used interpolation to determine the motion of celestial bodies from periodic observations. Notable mathematicians like Gauss, Newton, Bessel, and Stirling made significant contributions to the field.2 Modern applications include weather forecasting, where interpolation is used to estimate values at grid points from data collected at scattered weather stations.

Refer to 1.1 and look for interpolation for more info.

A new function has to be formed which is very close to the original function, both these functions have to agree on the tabulated values. 

**<u>Weierstrass Theorem</u>** is stated as : if f(x) is continuous in x<sub>0</sub> <= x <= x<sub>n</sub> then given any $\epsilon >0$, there exists a polynomial P(x) such that $|f(x) - P(x)| < \epsilon$ for all x in (x<sub>0</sub>, x<sub>n</sub>).

Questions that are out of the scope of the book but are important include :

1. How should the closeness of the approximation be measured?

2. What is the criterion to decide the best polynomial approximation to the function?

# TODO : Start from 3.2 Pg - 74 (edit when start)
