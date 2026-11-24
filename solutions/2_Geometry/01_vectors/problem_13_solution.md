# Exercise 13 – Do Four Points Lie in One Plane?

## Problem Statement

Given

$$
A=(0,0,0),\qquad B=(1,2,0),\qquad C=(0,1,1),\qquad D=(2,5,1).
$$

1. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$.
2. Find $n=\overrightarrow{AB}\times\overrightarrow{AC}$.
3. Construct $\overrightarrow{AD}$ and check whether $\overrightarrow{AD}\cdot n=0$.
4. Based on this, decide whether $D$ lies in the plane determined by $A,B,C$, and justify the criterion.

## Solution

### 1. Constructing $\overrightarrow{AB}$ and $\overrightarrow{AC}$

Using $A = (0, 0, 0)$ as the reference point, we construct the two vectors spanning the plane through $A$, $B$, and $C$:

$$
\overrightarrow{AB} = B - A = (1 - 0,\, 2 - 0,\, 0 - 0) = (1, 2, 0)
$$

$$
\overrightarrow{AC} = C - A = (0 - 0,\, 1 - 0,\, 1 - 0) = (0, 1, 1)
$$

---

### 2. Finding the Normal Vector $n = \overrightarrow{AB} \times \overrightarrow{AC}$

We compute the cross product $\overrightarrow{AB} \times \overrightarrow{AC}$ to obtain a vector normal (perpendicular) to the plane determined by $A, B, C$:

$$
n = \overrightarrow{AB} \times \overrightarrow{AC} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 1 & 2 & 0 \\ 0 & 1 & 1 \end{vmatrix}
$$

Expanding by minors along the first row:

$$
n = \mathbf{i} \begin{vmatrix} 2 & 0 \\ 1 & 1 \end{vmatrix} - \mathbf{j} \begin{vmatrix} 1 & 0 \\ 0 & 1 \end{vmatrix} + \mathbf{k} \begin{vmatrix} 1 & 2 \\ 0 & 1 \end{vmatrix}
$$

$$
n = \bigl((2)(1) - (0)(1)\bigr)\mathbf{i} - \bigl((1)(1) - (0)(0)\bigr)\mathbf{j} + \bigl((1)(1) - (2)(0)\bigr)\mathbf{k}
$$

$$
n = 2\mathbf{i} - 1\mathbf{j} + 1\mathbf{k} = (2, -1, 1)
$$

---

### 3. Constructing $\overrightarrow{AD}$ and Checking $\overrightarrow{AD} \cdot n = 0$

First, construct the displacement vector from $A = (0, 0, 0)$ to $D = (2, 5, 1)$:

$$
\overrightarrow{AD} = D - A = (2 - 0,\, 5 - 0,\, 1 - 0) = (2, 5, 1)
$$

Next, compute the dot product $\overrightarrow{AD} \cdot n$:

$$
\overrightarrow{AD} \cdot n = (2)(2) + (5)(-1) + (1)(1) = 4 - 5 + 1 = 0
$$

The dot product is indeed equal to $0$.

---

### 4. Decision on Coplanarity and Justification of the Criterion

- **Decision:**  
  Since $\overrightarrow{AD} \cdot n = 0$, the point $D = (2, 5, 1)$ **does lie** in the plane determined by $A, B,$ and $C$ (all four points are coplanar).

- **Justification of the Criterion:**  
  - Because $n = \overrightarrow{AB} \times \overrightarrow{AC} = (2, -1, 1)$ is non-zero, $A, B,$ and $C$ are non-collinear and uniquely define a plane $\Pi$ passing through $A$, with $n$ perpendicular to every vector lying inside $\Pi$.
  - A point $D$ lies on $\Pi$ if and only if the displacement vector $\overrightarrow{AD}$ lies inside $\Pi$, which occurs precisely when $\overrightarrow{AD}$ is perpendicular to the plane's normal vector $n$ ($\overrightarrow{AD} \cdot n = 0$).
  - Geometrically, the scalar triple product $\overrightarrow{AD} \cdot (\overrightarrow{AB} \times \overrightarrow{AC}) = 0$ means the parallelepiped spanned by $\overrightarrow{AB}, \overrightarrow{AC},$ and $\overrightarrow{AD}$ has zero volume, proving the three vectors lie in a single flat plane. (In fact, $\overrightarrow{AD} = 2\overrightarrow{AB} + 1\overrightarrow{AC}$.)