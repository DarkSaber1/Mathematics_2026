# Exercise 12 – A Normal Vector to a Plane

## Problem Statement

Given $A=(1,0,2)$, $B=(2,1,0)$, and $C=(0,3,1)$. Construct two vectors lying in the plane, find a vector perpendicular to both, and check the perpendicularity using dot products.

## Solution

### 1. Constructing Two Vectors Lying in the Plane

Since points $A = (1, 0, 2)$, $B = (2, 1, 0)$, and $C = (0, 3, 1)$ all lie in the plane, any displacement vector connecting two of these points lies completely within the plane. Using $A$ as a common initial point, we construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$:

$$
\overrightarrow{AB} = B - A = (2 - 1,\, 1 - 0,\, 0 - 2) = (1, 1, -2)
$$

$$
\overrightarrow{AC} = C - A = (0 - 1,\, 3 - 0,\, 1 - 2) = (-1, 3, -1)
$$

Since $(1, 1, -2)$ and $(-1, 3, -1)$ are not scalar multiples of one another, they are linearly independent and span the plane.

---

### 2. Finding a Normal Vector $n$ Perpendicular to Both Vectors

In $\mathbb{R}^3$, the cross product of two non-parallel vectors produces a vector $n$ that is simultaneously perpendicular (normal) to both vectors—and hence perpendicular to the entire plane:

$$
n = \overrightarrow{AB} \times \overrightarrow{AC} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 1 & 1 & -2 \\ -1 & 3 & -1 \end{vmatrix}
$$

Expanding the determinant along the first row:

$$
n = \mathbf{i} \begin{vmatrix} 1 & -2 \\ 3 & -1 \end{vmatrix} - \mathbf{j} \begin{vmatrix} 1 & -2 \\ -1 & -1 \end{vmatrix} + \mathbf{k} \begin{vmatrix} 1 & 1 \\ -1 & 3 \end{vmatrix}
$$

$$
n = \bigl((1)(-1) - (-2)(3)\bigr)\mathbf{i} - \bigl((1)(-1) - (-2)(-1)\bigr)\mathbf{j} + \bigl((1)(3) - (1)(-1)\bigr)\mathbf{k}
$$

$$
n = (-1 + 6)\mathbf{i} - (-1 - 2)\mathbf{j} + (3 + 1)\mathbf{k} = 5\mathbf{i} + 3\mathbf{j} + 4\mathbf{k} = (5, 3, 4)
$$

Thus, a normal vector to the plane is:

$$
n = (5, 3, 4)
$$

---

### 3. Checking Perpendicularity Using Dot Products

We verify that $n = (5, 3, 4)$ is perpendicular to both $\overrightarrow{AB}$ and $\overrightarrow{AC}$ by computing their dot products:

- **Dot product with $\overrightarrow{AB} = (1, 1, -2)$:**

$$
n \cdot \overrightarrow{AB} = (5)(1) + (3)(1) + (4)(-2) = 5 + 3 - 8 = 0
$$

- **Dot product with $\overrightarrow{AC} = (-1, 3, -1)$:**

$$
n \cdot \overrightarrow{AC} = (5)(-1) + (3)(3) + (4)(-1) = -5 + 9 - 4 = 0
$$

Since both dot products equal $0$, the vector $n = (5, 3, 4)$ is confirmed to be perpendicular to both in-plane vectors and therefore serves as a valid normal vector to the plane passing through $A$, $B$, and $C$.