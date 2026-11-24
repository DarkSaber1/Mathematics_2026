# Exercise 1 – Vector Operations and Their Meaning

## Problem Statement

For $u=(2,-1,3)$ and $v=(-1,4,2)$ compute

$$
u+v,\qquad u-v,\qquad 3u-2v.
$$

Then verify that $(u+v)-v=u$, and explain geometrically what adding two vectors means.

## Solution

### 1. Computing Vector Operations

Vector addition, subtraction, and scalar multiplication in $\mathbb{R}^3$ are performed component-wise. Given:

$$
u = (2, -1, 3), \qquad v = (-1, 4, 2)
$$

- **Vector Addition ($u + v$):**

$$
u + v = (2 + (-1),\, -1 + 4,\, 3 + 2) = (1, 3, 5)
$$

- **Vector Subtraction ($u - v$):**

$$
u - v = (2 - (-1),\, -1 - 4,\, 3 - 2) = (3, -5, 1)
$$

- **Linear Combination ($3u - 2v$):**  
  First, compute the scalar multiples $3u$ and $2v$:

$$
3u = 3(2, -1, 3) = (6, -3, 9)
$$

$$
2v = 2(-1, 4, 2) = (-2, 8, 4)
$$

  Now subtract the resulting vectors component-wise:

$$
3u - 2v = (6 - (-2),\, -3 - 8,\, 9 - 4) = (8, -11, 5)
$$

---

### 2. Verifying $(u + v) - v = u$

Using our previously computed result $u + v = (1, 3, 5)$, we subtract $v = (-1, 4, 2)$:

$$
(u + v) - v = (1 - (-1),\, 3 - 4,\, 5 - 2) = (2, -1, 3)
$$

Since $(2, -1, 3)$ matches the original vector $u$, the identity $(u + v) - v = u$ is verified.

---

### 3. Geometric Meaning of Vector Addition

Geometrically, adding two vectors $u$ and $v$ represents the **net displacement** obtained by applying one displacement immediately after the other. This can be visualized in two equivalent ways:

- **Triangle Rule (Tip-to-Tail Method):**  
  Place the tail (starting point) of vector $v$ at the tip (endpoint) of vector $u$. The sum $u + v$ is the single directed line segment drawn from the tail of $u$ directly to the tip of $v$.

- **Parallelogram Rule:**  
  When $u$ and $v$ are drawn starting from the same initial point (such as the origin), they form two adjacent sides of a parallelogram. The sum $u + v$ corresponds to the main diagonal of that parallelogram starting from the common origin.