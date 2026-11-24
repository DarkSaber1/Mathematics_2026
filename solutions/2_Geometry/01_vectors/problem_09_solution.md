# Exercise 9 – Cross Product as a Perpendicular Direction

## Problem Statement

For $u=(1,2,0)$ and $v=(0,1,3)$ compute $u\times v$. Use dot products to check perpendicularity to both vectors, compute $v\times u$, and compare the results.

## Solution

### 1. Computing the Cross Product $u \times v$

For two vectors $u = (u_1, u_2, u_3)$ and $v = (v_1, v_2, v_3)$ in $\mathbb{R}^3$, the cross product $u \times v$ is computed using the $3 \times 3$ determinant expansion along the standard basis vectors $\mathbf{i}, \mathbf{j}, \mathbf{k}$:

$$
u \times v = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 1 & 2 & 0 \\ 0 & 1 & 3 \end{vmatrix}
$$

Expanding by minors:

$$
u \times v = \mathbf{i} \begin{vmatrix} 2 & 0 \\ 1 & 3 \end{vmatrix} - \mathbf{j} \begin{vmatrix} 1 & 0 \\ 0 & 3 \end{vmatrix} + \mathbf{k} \begin{vmatrix} 1 & 2 \\ 0 & 1 \end{vmatrix}
$$

$$
u \times v = ((2)(3) - (0)(1))\mathbf{i} - ((1)(3) - (0)(0))\mathbf{j} + ((1)(1) - (2)(0))\mathbf{k}
$$

$$
u \times v = 6\mathbf{i} - 3\mathbf{j} + 1\mathbf{k} = (6, -3, 1)
$$

---

### 2. Checking Perpendicularity Using Dot Products

A vector is perpendicular (orthogonal) to both $u$ and $v$ if its dot product with each vector equals $0$.

- **Dot product with $u = (1, 2, 0)$:**

$$
(u \times v) \cdot u = (6)(1) + (-3)(2) + (1)(0) = 6 - 6 + 0 = 0
$$

- **Dot product with $v = (0, 1, 3)$:**

$$
(u \times v) \cdot v = (6)(0) + (-3)(1) + (1)(3) = 0 - 3 + 3 = 0
$$

Since both dot products equal $0$, the vector $u \times v = (6, -3, 1)$ is confirmed to be perpendicular to both $u$ and $v$ (and therefore normal to the plane they span).

---

### 3. Computing $v \times u$

Reversing the order of the vectors swaps the second and third rows of the determinant:

$$
v \times u = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 0 & 1 & 3 \\ 1 & 2 & 0 \end{vmatrix}
$$

Expanding by minors:

$$
v \times u = \mathbf{i} \begin{vmatrix} 1 & 3 \\ 2 & 0 \end{vmatrix} - \mathbf{j} \begin{vmatrix} 0 & 3 \\ 1 & 0 \end{vmatrix} + \mathbf{k} \begin{vmatrix} 0 & 1 \\ 1 & 2 \end{vmatrix}
$$

$$
v \times u = ((1)(0) - (3)(2))\mathbf{i} - ((0)(0) - (3)(1))\mathbf{j} + ((0)(2) - (1)(1))\mathbf{k}
$$

$$
v \times u = -6\mathbf{i} + 3\mathbf{j} - 1\mathbf{k} = (-6, 3, -1)
$$

---

### 4. Comparing $u \times v$ and $v \times u$

Comparing the two resulting vectors shows that they are exact opposites of one another:

$$
v \times u = (-6, 3, -1) = -(6, -3, 1) = -(u \times v)
$$

- **Anti-Commutativity:** Unlike scalar multiplication or the dot product, the cross product is **anti-commutative** ($v \times u = -(u \times v)$).
- **Geometric Interpretation (Right-Hand Rule):** Both vectors have the exact same length ($\sqrt{6^2 + (-3)^2 + 1^2} = \sqrt{46}$) and lie along the exact same line perpendicular to the plane of $u$ and $v$, but reversing the order of the arguments flips the orientation by $180^\circ$ to point in the opposite direction.