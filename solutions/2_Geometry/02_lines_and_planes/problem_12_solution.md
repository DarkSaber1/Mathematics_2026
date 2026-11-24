# Exercise 12 – Intersection Line of Two Planes

## Problem Statement

Find a parametric equation of the line that is the intersection of

$$
x+y+z=3,\qquad x-y+z=1.
$$

Find its direction vector in two ways: from the system of equations and from the cross product of the normal vectors. Compare the results.

## Solution

### 1. Algebraic Approach: Solving the System of Plane Equations

A point $(x, y, z)$ lies on the intersection line if and only if it simultaneously satisfies both plane equations:

$$
\begin{cases}
x + y + z = 3 \\
x - y + z = 1
\end{cases}
$$

- **Step 1: Find $y$ by subtracting the second equation from the first:**

$$
(x + y + z) - (x - y + z) = 3 - 1 \implies 2y = 2 \implies y = 1
$$

- **Step 2: Substitute $y = 1$ back into the first equation:**

$$
x + 1 + z = 3 \implies x + z = 2
$$

- **Step 3: Introduce a free parameter $t \in \mathbb{R}$:**  
  Let $z = t$. Then $x = 2 - t$ and $y = 1$. Writing this in vector parametric form gives the intersection line $L$:

$$
L : (x, y, z) = (2, 1, 0) + t(-1, 0, 1) \qquad (t \in \mathbb{R})
$$

From this parametric representation, the direction vector obtained algebraically is:

$$
v_{\text{alg}} = (-1, 0, 1)
$$

---

### 2. Geometric Approach: Cross Product of the Normal Vectors

The intersection line $L$ lies inside both planes simultaneously, meaning its direction vector must be perpendicular to both planes' normal vectors:

$$
n_1 = (1, 1, 1), \qquad n_2 = (1, -1, 1)
$$

We compute a geometric direction vector $v_{\text{geo}} = n_1 \times n_2$:

$$
v_{\text{geo}} = n_1 \times n_2 = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 1 & 1 & 1 \\ 1 & -1 & 1 \end{vmatrix}
$$

Expanding by minors along the first row:

$$
v_{\text{geo}} = \mathbf{i} \begin{vmatrix} 1 & 1 \\ -1 & 1 \end{vmatrix} - \mathbf{j} \begin{vmatrix} 1 & 1 \\ 1 & 1 \end{vmatrix} + \mathbf{k} \begin{vmatrix} 1 & 1 \\ 1 & -1 \end{vmatrix}
$$

$$
v_{\text{geo}} = \bigl((1)(1) - (1)(-1)\bigr)\mathbf{i} - \bigl((1)(1) - (1)(1)\bigr)\mathbf{j} + \bigl((1)(-1) - (1)(1)\bigr)\mathbf{k}
$$

$$
v_{\text{geo}} = 2\mathbf{i} - 0\mathbf{j} - 2\mathbf{k} = (2, 0, -2)
$$

---

### 3. Comparing the Two Direction Vectors

Comparing $v_{\text{alg}}$ and $v_{\text{geo}}$:

$$
v_{\text{alg}} = (-1, 0, 1), \qquad v_{\text{geo}} = (2, 0, -2) = -2(-1, 0, 1) = -2\,v_{\text{alg}}
$$

The two direction vectors are **non-zero scalar multiples of one another** ($v_{\text{geo}} = -2v_{\text{alg}}$). Geometrically, this means both methods describe the **exact same spatial direction** (parallel to the same line in $\mathbb{R}^3$), differing only in length (by a factor of $2$) and orientation (opposite sign), which is completely expected since a line's direction vector is unique only up to a non-zero scalar factor.