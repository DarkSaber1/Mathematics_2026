# Exercise 8 – Sphere

## Problem Statement

Reduce

$$
x^2+y^2+z^2-4x+2y-6z-2=0
$$

to canonical form. Find the center and radius. Give two points on the sphere and check them in the equation.

## Solution

### 1. Reducing to Canonical Form by Completing the Square

Start with the general equation of the sphere in $\mathbb{R}^3$:

$$
x^2 + y^2 + z^2 - 4x + 2y - 6z - 2 = 0
$$

Group the $x$-, $y$-, and $z$-terms separately and move the constant $-2$ to the right-hand side:

$$
(x^2 - 4x) + (y^2 + 2y) + (z^2 - 6z) = 2
$$

Complete the square for each of the three variables:
- For $x^2 - 4x$: add $(-2)^2 = 4$.
- For $y^2 + 2y$: add $(1)^2 = 1$.
- For $z^2 - 6z$: add $(-3)^2 = 9$.

Add $4 + 1 + 9 = 14$ to both sides of the equation:

$$
(x^2 - 4x + 4) + (y^2 + 2y + 1) + (z^2 - 6z + 9) = 2 + 4 + 1 + 9
$$

Factor each quadratic trinomial into a squared binomial to obtain the **canonical form** $(x - x_0)^2 + (y - y_0)^2 + (z - z_0)^2 = r^2$:

$$
(x - 2)^2 + (y + 1)^2 + (z - 3)^2 = 16
$$

---

### 2. Center and Radius

Comparing $(x - 2)^2 + (y - (-1))^2 + (z - 3)^2 = 4^2$ with the standard sphere equation $(x - x_0)^2 + (y - y_0)^2 + (z - z_0)^2 = r^2$:

- **Center:** $(x_0, y_0, z_0) = (2, -1, 3)$
- **Radius:** $r = \sqrt{16} = 4$

---

### 3. Finding Two Points on the Sphere and Checking Them in the Equation

Starting from the center $(2, -1, 3)$ and moving $r = 4$ units in the positive and negative $x$-directions produces two simple points on the sphere:

- **Point 1:** $P_1 = (2 + 4,\, -1,\, 3) = (6, -1, 3)$
- **Point 2:** $P_2 = (2 - 4,\, -1,\, 3) = (-2, -1, 3)$

#### Verification in Canonical Form: $(x - 2)^2 + (y + 1)^2 + (z - 3)^2 = 16$

- **For $P_1 = (6, -1, 3)$:**

$$
(6 - 2)^2 + (-1 + 1)^2 + (3 - 3)^2 = 4^2 + 0^2 + 0^2 = 16 \quad (\text{True})
$$

- **For $P_2 = (-2, -1, 3)$:**

$$
(-2 - 2)^2 + (-1 + 1)^2 + (3 - 3)^2 = (-4)^2 + 0^2 + 0^2 = 16 \quad (\text{True})
$$

#### Verification in General Form: $x^2 + y^2 + z^2 - 4x + 2y - 6z - 2 = 0$

- **For $P_1 = (6, -1, 3)$:**

$$
6^2 + (-1)^2 + 3^2 - 4(6) + 2(-1) - 6(3) - 2 = 36 + 1 + 9 - 24 - 2 - 18 - 2 = 46 - 46 = 0 \quad (\text{True})
$$

- **For $P_2 = (-2, -1, 3)$:**

$$
(-2)^2 + (-1)^2 + 3^2 - 4(-2) + 2(-1) - 6(3) - 2 = 4 + 1 + 9 + 8 - 2 - 18 - 2 = 22 - 22 = 0 \quad (\text{True})
$$

Both points satisfy both equations, verifying our center, radius, and canonical form.