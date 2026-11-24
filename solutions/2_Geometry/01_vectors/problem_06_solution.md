# Exercise 6 – Projection and Perpendicular Component

## Problem Statement

Find the projection of $u=(4,2)$ onto the direction $v=(1,1)$. Then compute

$$
r=u-\mathrm{proj}_v\,u
$$

and verify that $r\cdot v=0$. Explain this result geometrically.

## Solution

### 1. Computing the Orthogonal Projection $\mathrm{proj}_v\,u$

The orthogonal projection of a vector $u$ onto a non-zero vector $v$ is given by the formula:

$$
\mathrm{proj}_v\,u = \frac{u \cdot v}{v \cdot v} v = \frac{u \cdot v}{\|v\|^2} v
$$

Given $u = (4, 2)$ and $v = (1, 1)$, we first compute the required dot products:

$$
u \cdot v = (4)(1) + (2)(1) = 4 + 2 = 6
$$

$$
v \cdot v = (1)(1) + (1)(1) = 1 + 1 = 2
$$

Substituting these values into the projection formula:

$$
\mathrm{proj}_v\,u = \frac{6}{2} (1, 1) = 3(1, 1) = (3, 3)
$$

---

### 2. Computing the Remainder Vector $r = u - \mathrm{proj}_v\,u$

Next, we subtract the projection vector $\mathrm{proj}_v\,u = (3, 3)$ from the original vector $u = (4, 2)$:

$$
r = u - \mathrm{proj}_v\,u = (4, 2) - (3, 3) = (4 - 3,\, 2 - 3) = (1, -1)
$$

---

### 3. Verifying That $r \cdot v = 0$

We test whether $r = (1, -1)$ is perpendicular to $v = (1, 1)$ by computing their dot product:

$$
r \cdot v = (1)(1) + (-1)(1) = 1 - 1 = 0
$$

Since $r \cdot v = 0$, the remainder vector $r$ is confirmed to be perpendicular (orthogonal) to the direction vector $v$.

---

### 4. Geometric Explanation

Geometrically, computing $\mathrm{proj}_v\,u$ drops a perpendicular line from the tip of $u = (4, 2)$ onto the line spanned by $v = (1, 1)$ (the line $y = x$).

- **Parallel Component ($\mathrm{proj}_v\,u = (3, 3)$):** This is the "shadow" of $u$ cast onto the line in the direction of $v$.
- **Perpendicular Component ($r = (1, -1)$):** This is the shortest vector connecting the line of $v$ directly to the tip of $u$, forming a $90^\circ$ right angle with $v$.

Together, $\mathrm{proj}_v\,u$ and $r$ form the two perpendicular legs of a right triangle whose hypotenuse is $u$, decomposing $u$ into $u = \mathrm{proj}_v\,u + r$.