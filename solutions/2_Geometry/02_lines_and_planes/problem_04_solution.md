# Exercise 4 – Plane Through Three Points

## Problem Statement

Find the equation of the plane through

$$
A=(1,0,0),\quad B=(0,1,0),\quad C=(0,0,1).
$$

First construct two vectors lying in the plane, and then use the cross product. Check the resulting equation on all three points.

## Solution

### 1. Constructing Two Vectors Lying in the Plane

Using $A = (1, 0, 0)$ as the common initial point, we construct two displacement vectors connecting $A$ to $B = (0, 1, 0)$ and $C = (0, 0, 1)$:

$$
\overrightarrow{AB} = B - A = (0 - 1,\, 1 - 0,\, 0 - 0) = (-1, 1, 0)
$$

$$
\overrightarrow{AC} = C - A = (0 - 1,\, 0 - 0,\, 1 - 0) = (-1, 0, 1)
$$

Since $\overrightarrow{AB}$ and $\overrightarrow{AC}$ are not scalar multiples of one another, they are linearly independent and span the plane.

---

### 2. Finding a Normal Vector Using the Cross Product

A normal vector $n$ perpendicular to the plane is given by the cross product $\overrightarrow{AB} \times \overrightarrow{AC}$:

$$
n = \overrightarrow{AB} \times \overrightarrow{AC} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ -1 & 1 & 0 \\ -1 & 0 & 1 \end{vmatrix}
$$

Expanding the determinant along the first row:

$$
n = \mathbf{i} \begin{vmatrix} 1 & 0 \\ 0 & 1 \end{vmatrix} - \mathbf{j} \begin{vmatrix} -1 & 0 \\ -1 & 1 \end{vmatrix} + \mathbf{k} \begin{vmatrix} -1 & 1 \\ -1 & 0 \end{vmatrix}
$$

$$
n = \bigl((1)(1) - (0)(0)\bigr)\mathbf{i} - \bigl((-1)(1) - (0)(-1)\bigr)\mathbf{j} + \bigl((-1)(0) - (1)(-1)\bigr)\mathbf{k}
$$

$$
n = 1\mathbf{i} - (-1)\mathbf{j} + 1\mathbf{k} = (1, 1, 1)
$$

---

### 3. Writing the Equation of the Plane

Using the point-normal equation $n \cdot (X - A) = 0$ with $n = (1, 1, 1)$ and $A = (1, 0, 0)$:

$$
1(x - 1) + 1(y - 0) + 1(z - 0) = 0
$$

$$
x - 1 + y + z = 0 \implies x + y + z = 1
$$

*(Or in general form: $x + y + z - 1 = 0$.)*

---

### 4. Checking the Resulting Equation on All Three Points

We substitute the coordinates of $A$, $B$, and $C$ into $x + y + z = 1$:

- **For $A = (1, 0, 0)$:**

$$
1 + 0 + 0 = 1 \quad (\text{True})
$$

- **For $B = (0, 1, 0)$:**

$$
0 + 1 + 0 = 1 \quad (\text{True})
$$

- **For $C = (0, 0, 1)$:**

$$
0 + 0 + 1 = 1 \quad (\text{True})
$$

All three points satisfy the equation, confirming that $x + y + z = 1$ is the unique plane passing through $A, B,$ and $C$.