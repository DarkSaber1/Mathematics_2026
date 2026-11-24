# Exercise 7 – Classifying a Second-Degree Equation

## Problem Statement

Determine the type of object described by:

1. $4x^2+9y^2=36$,
2. $x^2-y^2=1$,
3. $x^2-4y=0$,
4. $x^2+y^2+1=0$.

In the last case, explain why there are no real points.

## Solution

### 1. Equation 1: $4x^2 + 9y^2 = 36$ (Ellipse)

Divide both sides of the equation by $36$ to put it into canonical form:

$$
\frac{4x^2}{36} + \frac{9y^2}{36} = 1 \implies \frac{x^2}{9} + \frac{y^2}{4} = 1
$$

- **Classification:** **Ellipse** centered at $(0, 0)$ with semiaxis lengths $a = 3$ (along the $x$-axis) and $b = 2$ (along the $y$-axis), because both quadratic terms are positive with distinct denominators and sum to $1$.

---

### 2. Equation 2: $x^2 - y^2 = 1$ (Equilateral / Rectangular Hyperbola)

This equation is already in canonical hyperbola form $\frac{x^2}{1^2} - \frac{y^2}{1^2} = 1$:

$$
x^2 - y^2 = 1
$$

- **Classification:** **Hyperbola** (specifically an equilateral hyperbola) centered at $(0, 0)$ with vertices at $(\pm 1, 0)$ and perpendicular asymptotes $y = \pm x$, because $x^2$ and $y^2$ appear with opposite signs and equal a positive constant.

---

### 3. Equation 3: $x^2 - 4y = 0$ (Parabola)

Isolate the squared variable $x^2$ on the left-hand side:

$$
x^2 = 4y
$$

- **Classification:** **Parabola** with vertex at $(0, 0)$, vertical axis of symmetry along the $y$-axis ($x = 0$), and opening upward (in the positive $y$-direction, since $y = \frac{x^2}{4} \ge 0$), because one variable is squared while the other appears linearly.

---

### 4. Equation 4: $x^2 + y^2 + 1 = 0$ (Empty Set / No Real Locus)

Rearrange the equation by moving $1$ to the right-hand side:

$$
x^2 + y^2 = -1
$$

- **Classification:** **Empty set ($\emptyset$)** — the equation describes no real geometric curve in the Euclidean plane $\mathbb{R}^2$.
- **Why There Are No Real Points:**  
  For every pair of real numbers $(x, y) \in \mathbb{R}^2$, the square of any real number is non-negative:

$$
x^2 \ge 0 \qquad \text{and} \qquad y^2 \ge 0
$$

  Adding two non-negative quantities always yields a non-negative sum:

$$
x^2 + y^2 \ge 0
$$

  Since $0 > -1$, the left-hand side $x^2 + y^2$ can never equal $-1$ for any real coordinates $(x, y)$, meaning the solution set in $\mathbb{R}^2$ is completely empty.