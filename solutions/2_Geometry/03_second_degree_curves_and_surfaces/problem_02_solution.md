# Exercise 2 – Circle by Completing the Square

## Problem Statement

Reduce

$$
x^2+y^2-6x+4y-3=0
$$

to canonical form. Find the center and radius, then substitute two simple points from the circle into both forms of the equation.

## Solution

### 1. Reducing to Canonical Form by Completing the Square

We start with the general equation of the circle:

$$
x^2 + y^2 - 6x + 4y - 3 = 0
$$

Group the $x$-terms and $y$-terms together, and move the constant term to the right-hand side:

$$
(x^2 - 6x) + (y^2 + 4y) = 3
$$

Complete the square for each variable separately:
- For $x^2 - 6x$: take half of $-6$ (which is $-3$) and square it to get $(-3)^2 = 9$.
- For $y^2 + 4y$: take half of $4$ (which is $2$) and square it to get $2^2 = 4$.

Add both $9$ and $4$ to both sides of the equation to preserve equality:

$$
(x^2 - 6x + 9) + (y^2 + 4y + 4) = 3 + 9 + 4
$$

Factor each quadratic trinomial as a squared binomial to obtain the **canonical form** $(x - x_0)^2 + (y - y_0)^2 = r^2$:

$$
(x - 3)^2 + (y + 2)^2 = 16
$$

---

### 2. Finding the Center and Radius

Comparing $(x - 3)^2 + (y - (-2))^2 = 4^2$ with the standard circle equation $(x - x_0)^2 + (y - y_0)^2 = r^2$:

- **Center:** $(x_0, y_0) = (3, -2)$
- **Radius:** $r = \sqrt{16} = 4$

---

### 3. Finding Two Simple Points on the Circle and Checking Both Equations

Starting from the center $(3, -2)$ and moving $r = 4$ units horizontally to the right and left gives two simple points on the circle:

- **Point 1:** $P_1 = (3 + 4,\, -2) = (7, -2)$
- **Point 2:** $P_2 = (3 - 4,\, -2) = (-1, -2)$

#### Verification in Canonical Form: $(x - 3)^2 + (y + 2)^2 = 16$

- **For $P_1 = (7, -2)$:**

$$
(7 - 3)^2 + (-2 + 2)^2 = 4^2 + 0^2 = 16 \quad (\text{True})
$$

- **For $P_2 = (-1, -2)$:**

$$
(-1 - 3)^2 + (-2 + 2)^2 = (-4)^2 + 0^2 = 16 \quad (\text{True})
$$

#### Verification in General Form: $x^2 + y^2 - 6x + 4y - 3 = 0$

- **For $P_1 = (7, -2)$:**

$$
7^2 + (-2)^2 - 6(7) + 4(-2) - 3 = 49 + 4 - 42 - 8 - 3 = 53 - 53 = 0 \quad (\text{True})
$$

- **For $P_2 = (-1, -2)$:**

$$
(-1)^2 + (-2)^2 - 6(-1) + 4(-2) - 3 = 1 + 4 + 6 - 8 - 3 = 11 - 11 = 0 \quad (\text{True})
$$

Both points satisfy both forms of the equation, confirming our reduction.