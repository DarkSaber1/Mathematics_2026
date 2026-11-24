# Exercise 11 – Plane Containing a Line and a Point

## Problem Statement

Find the equation of the plane containing

$$
(x,y,z)=(1,0,2)+t(1,1,-1)
$$

and the point $P=(0,2,1)$. Check that both the entire line and the point lie in the plane you obtain.

## Solution

### 1. Constructing Two Linearly Independent Direction Vectors in the Plane

To determine a plane in $\mathbb{R}^3$, we need a point in the plane and two non-parallel vectors lying inside it:

- **First vector ($v_1$):** Since the entire line $(x, y, z) = (1, 0, 2) + t(1, 1, -1)$ lies in the plane, its direction vector $v_1$ lies parallel to (and within) the plane, and its base point $Q = (1, 0, 2)$ lies on the plane:

$$
Q = (1, 0, 2), \qquad v_1 = (1, 1, -1)
$$

- **Second vector ($v_2$):** Since both $Q = (1, 0, 2)$ and $P = (0, 2, 1)$ lie in the plane, the displacement vector $\overrightarrow{QP}$ connecting them also lies inside the plane:

$$
v_2 = \overrightarrow{QP} = P - Q = (0 - 1,\, 2 - 0,\, 1 - 2) = (-1, 2, -1)
$$

Since $v_1 = (1, 1, -1)$ and $v_2 = (-1, 2, -1)$ are not scalar multiples of each other, they are linearly independent.

---

### 2. Finding a Normal Vector $n$ via the Cross Product

A normal vector $n$ perpendicular to the plane is given by the cross product $v_1 \times v_2$:

$$
n = v_1 \times v_2 = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 1 & 1 & -1 \\ -1 & 2 & -1 \end{vmatrix}
$$

Expanding by minors along the first row:

$$
n = \mathbf{i} \begin{vmatrix} 1 & -1 \\ 2 & -1 \end{vmatrix} - \mathbf{j} \begin{vmatrix} 1 & -1 \\ -1 & -1 \end{vmatrix} + \mathbf{k} \begin{vmatrix} 1 & 1 \\ -1 & 2 \end{vmatrix}
$$

$$
n = \bigl((1)(-1) - (-1)(2)\bigr)\mathbf{i} - \bigl((1)(-1) - (-1)(-1)\bigr)\mathbf{j} + \bigl((1)(2) - (1)(-1)\bigr)\mathbf{k}
$$

$$
n = (-1 + 2)\mathbf{i} - (-1 - 1)\mathbf{j} + (2 + 1)\mathbf{k} = 1\mathbf{i} + 2\mathbf{j} + 3\mathbf{k} = (1, 2, 3)
$$

---

### 3. Writing the Equation of the Plane

Using the point-normal form $n \cdot (X - Q) = 0$ with $n = (1, 2, 3)$ and $Q = (1, 0, 2)$:

$$
1(x - 1) + 2(y - 0) + 3(z - 2) = 0
$$

$$
x - 1 + 2y + 3z - 6 = 0 \implies x + 2y + 3z = 7
$$

*(Or in general form: $x + 2y + 3z - 7 = 0$.)*

---

### 4. Checking That Both the Point $P$ and the Entire Line Lie in the Plane

- **Verification for Point $P = (0, 2, 1)$:**  
  Substitute $x = 0$, $y = 2$, and $z = 1$ into $x + 2y + 3z = 7$:

$$
0 + 2(2) + 3(1) = 0 + 4 + 3 = 7 \quad (\text{True})
$$

- **Verification for the Entire Line $(x, y, z) = (1 + t,\, t,\, 2 - t)$:**  
  Substitute the general parametric point $(1 + t,\, t,\, 2 - t)$ for arbitrary $t \in \mathbb{R}$ into $x + 2y + 3z = 7$:

$$
(1 + t) + 2(t) + 3(2 - t) = 1 + t + 2t + 6 - 3t = (1 + 6) + (t + 2t - 3t) = 7 + 0t = 7
$$

Because the identity $7 = 7$ holds for **every** real value of $t \in \mathbb{R}$, every point of the line lies in the plane, confirming that both the entire line and point $P$ are contained in $x + 2y + 3z = 7$.