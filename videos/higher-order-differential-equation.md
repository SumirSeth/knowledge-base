---
title: 'Pieces of Information about Higher Order DE'
description: 'Compilation of video notes from *The Math Sorcerer*'
video: 'https://www.youtube.com/playlist?list=PLO1y6V1SXjjOxAE4cqHXhD2dsO8cnlick'
playlist: 'https://www.youtube.com/playlist?list=PLO1y6V1SXjjOxAE4cqHXhD2dsO8cnlick'
tags: ['DE', 'Differential Equations', 'Math']
source: 'The Math Sorcerer'
---

> Important Topics that are not covered : `forcing function (input)`, `non-forcing function (input)`, `Wronskian`.

# Pieces of information about Higher Order DE

Higher order corresponds to the order of highest derivative ( $\frac{dy}{dx}$ typically ) which is more than 1.

It's typical form is of:

$b_0x\frac{d^ny}{dx^n} + b_1x\frac{d^{n-1}y}{dx^{n-1}}... + b_nxy = X$ where $X$ is a any function of $x$.

For <u>Homogeneous,</u> $X=0$.

The complete solution of such HODE is given as the sum of Complimentary Function *(CF)* and Partial Integral *(PI)*
$y = CF + PI$

### On solution of these DE

#### Homogeneous

These DEs can be solved by `IDOM` : Inverse Differential Operator Method. Follow the four cases for the roots of auxillary eq :

- If roots are real and distinct

- If roots are real and some/all roots are non-distinct

- If roots are complex and distinct

- If roots are complex and some/all roots are non-distinct

These methods will give the CF. CF's containt arbitrary constants which is in contrast to PI's.

#### Non-Homogeneous

These DE's can be solved by incorporating `IDOM` and `VOPM`: Varitation of Parameters. Generally, follow the four cases in context of what the `X` (RHS) involves.

- If $X = e^{ax}$

- If $X = sin(ax \pm b)$ or $X =cos(ax \pm b)$

- If $X =\phi(x)$ where $\phi(x)$ is an algebraic function

- If $X =e^{ax}v$ where `v` is a function of x.

For DE's of the form $y''+py' + qy = X$ we can also use `VOPM`.

#### DE's reducible to Linear DE with constant coefficiants

Use *Cauchy's DE* or *Legendre's DE*.
