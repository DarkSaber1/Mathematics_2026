# Exercise 7 – Linear Dependence Without Heavy Computation

## Problem Statement

Given

$$
u=(1,2,3),\qquad v=(2,4,6),\qquad w=(0,1,1).
$$

Identify a specific relation between $u$ and $v$, decide whether the three vectors can be linearly independent, and explain why no long calculation is needed.

## Solution

### 1. Specific Relation Between $u$ and $v$

Comparing the components of $u = (1, 2, 3)$ and $v = (2, 4, 6)$ directly shows that every component of $v$ is exactly twice the corresponding component of $u$:

$$
v = 2(1, 2, 3) = 2u \qquad \left(\text{or equivalently, } 2u - v = \mathbf{0}\right)
$$

Thus, $v$ is a scalar multiple of $u$, meaning $u$ and $v$ are collinear (lie along the same line through the origin).

---

### 2. Decision on Linear Independence of $\{u, v, w\}$

The three vectors $u, v, w$ **cannot be linearly independent**; they are **linearly dependent**.

To show this explicitly via the definition of linear dependence, we can form a non-trivial linear combination equal to the zero vector $\mathbf{0} = (0, 0, 0)$ by choosing the scalars $c_1 = 2$, $c_2 = -1$, and $c_3 = 0$:

$$
2u - 1v + 0w = 2(1, 2, 3) - (2, 4, 6) + 0(0, 1, 1) = (0, 0, 0)
$$

Since not all scalar coefficients are zero ($c_1 = 2 \neq 0$ and $c_2 = -1 \neq 0$), the set $\{u, v, w\}$ is linearly dependent.

---

### 3. Why No Long Calculation Is Needed

No determinant calculation or Gaussian elimination on a $3 \times 3$ matrix is required because of a fundamental structural property of linear independence:

- **Subset Rule:** If a subset of vectors is already linearly dependent (here, $\{u, v\}$ is dependent because $v = 2u$), then **any larger set containing that subset is automatically linearly dependent**, regardless of what vector $w$ is added.
- **Geometric Perspective:** Because $v$ lies on the exact same line spanned by $u$, the pair $\{u, v\}$ spans only a $1$-dimensional line instead of a $2$-dimensional plane. Adding $w = (0, 1, 1)$ can at most span a $2$-dimensional plane in $\mathbb{R}^3$, never a full $3$-dimensional volume.