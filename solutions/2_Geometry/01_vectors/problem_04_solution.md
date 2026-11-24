# Exercise 4 – Dot Product and Perpendicularity

## Problem Statement

For $u=(1,2,-1)$ and $v=(2,-1,3)$ compute $u\cdot v$ and determine whether the vectors are perpendicular. Then find $a$ so that $w=(2,-1,a)$ is perpendicular to $u$, and check the result.

## Solution

### 1. Computing $u \cdot v$ and Testing Perpendicularity

The dot product (scalar product) of two vectors $u = (u_1, u_2, u_3)$ and $v = (v_1, v_2, v_3)$ in $\mathbb{R}^3$ is defined as:

$$
u \cdot v = u_1 v_1 + u_2 v_2 + u_3 v_3
$$

Substituting $u = (1, 2, -1)$ and $v = (2, -1, 3)$:

$$
u \cdot v = (1)(2) + (2)(-1) + (-1)(3) = 2 - 2 - 3 = -3
$$

**Perpendicularity Criterion:** Two non-zero vectors are perpendicular (orthogonal) if and only if their dot product equals $0$. Since $u \cdot v = -3 \neq 0$, the vectors $u$ and $v$ are **not perpendicular**.

---

### 2. Finding $a$ So That $w = (2, -1, a)$ Is Perpendicular to $u$

For $w = (2, -1, a)$ to be perpendicular to $u = (1, 2, -1)$, we set their dot product equal to zero:

$$
u \cdot w = 0
$$

Expanding the dot product:

$$
(1)(2) + (2)(-1) + (-1)(a) = 0
$$

$$
2 - 2 - a = 0
$$

$$
-a = 0 \implies a = 0
$$

Thus, the required vector is:

$$
w = (2, -1, 0)
$$

---

### 3. Checking the Result

We verify that $w = (2, -1, 0)$ is perpendicular to $u = (1, 2, -1)$ by computing $u \cdot w$ directly:

$$
u \cdot w = (1)(2) + (2)(-1) + (-1)(0) = 2 - 2 + 0 = 0
$$

Since $u \cdot w = 0$, the vector $w = (2, -1, 0)$ is confirmed to be perpendicular to $u$.