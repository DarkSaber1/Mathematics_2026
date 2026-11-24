# Exercise 8 – Linear Combination and Checking the Result

## Problem Statement

Check whether $w=(5,1)$ can be written as

$$
w=au+bv,
$$

where $u=(1,1)$ and $v=(2,-1)$. If so, find $a,b$, reconstruct $w$ from them, and explain the geometric meaning of the existence of such coefficients.

## Solution

### 1. Setting Up and Solving the Linear System for $a$ and $b$

We want to determine whether there exist real scalars $a$ and $b$ such that:

$$
a(1, 1) + b(2, -1) = (5, 1)
$$

Expanding the left-hand side component-wise gives:

$$
(a + 2b,\, a - b) = (5, 1)
$$

Equating corresponding coordinates yields a system of two linear equations:

$$
\begin{cases}
a + 2b = 5 \\
a - b = 1
\end{cases}
$$

Subtracting the second equation from the first eliminates $a$:

$$
(a + 2b) - (a - b) = 5 - 1 \implies 3b = 4 \implies b = \frac{4}{3}
$$

Substituting $b = \frac{4}{3}$ into the second equation $a - b = 1$:

$$
a - \frac{4}{3} = 1 \implies a = 1 + \frac{4}{3} = \frac{7}{3}
$$

Since a unique solution exists, $w$ **can** be written as a linear combination of $u$ and $v$ with:

$$
a = \frac{7}{3}, \qquad b = \frac{4}{3}
$$

---

### 2. Reconstructing $w$ from $a$ and $b$

We verify the result by substituting $a = \frac{7}{3}$ and $b = \frac{4}{3}$ back into $au + bv$:

$$
\frac{7}{3}u + \frac{4}{3}v = \frac{7}{3}(1, 1) + \frac{4}{3}(2, -1)
$$

$$
\frac{7}{3}u + \frac{4}{3}v = \left(\frac{7}{3},\, \frac{7}{3}\right) + \left(\frac{8}{3},\, -\frac{4}{3}\right) = \left(\frac{15}{3},\, \frac{3}{3}\right) = (5, 1) = w
$$

This reconstructs $w = (5, 1)$ exactly.

---

### 3. Geometric Meaning of the Existence of Such Coefficients

Geometrically, the existence of scalars $a$ and $b$ such that $w = au + bv$ means two things:

- **Spanning the Plane:** Because $u = (1, 1)$ and $v = (2, -1)$ do not lie on the same line (they are linearly independent and non-parallel), their directions form an oblique coordinate grid that spans the entire $\mathbb{R}^2$ plane. Consequently, **every** point or vector in $\mathbb{R}^2$ can be reached using a unique combination of steps along $u$ and $v$.
- **Path Construction:** To reach the target endpoint $(5, 1)$ starting from the origin, we move $\frac{7}{3}$ units along the direction of $u$ and then $\frac{4}{3}$ units along the direction of $v$ (forming the diagonal of a scaled parallelogram).