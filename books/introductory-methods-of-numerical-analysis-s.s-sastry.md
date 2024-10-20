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
