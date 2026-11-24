# Exercise 2 – Distance as the Length of a Vector

## Problem Statement

The points are $A=(1,2,3)$ and $B=(4,-2,6)$.

1. Construct $\overrightarrow{AB}$.
2. Compute its length.
3. Compute the distance between the points using the coordinate formula.
4. Explain why both calculations give the same result.

## Solution

### 1. Constructing the Displacement Vector $\overrightarrow{AB}$

To construct the vector $\overrightarrow{AB}$ pointing from initial point $A = (1, 2, 3)$ to terminal point $B = (4, -2, 6)$, we subtract the coordinates of $A$ from the corresponding coordinates of $B$:

$$
\overrightarrow{AB} = B - A = (4 - 1,\, -2 - 2,\, 6 - 3) = (3, -4, 3)
$$

---

### 2. Computing the Length of $\overrightarrow{AB}$

The length (Euclidean norm) of a vector $v = (v_1, v_2, v_3)$ in $\mathbb{R}^3$ is defined as $\|v\| = \sqrt{v_1^2 + v_2^2 + v_3^2}$. Applying this to $\overrightarrow{AB} = (3, -4, 3)$:

$$
\|\overrightarrow{AB}\| = \sqrt{3^2 + (-4)^2 + 3^2} = \sqrt{9 + 16 + 9} = \sqrt{34}
$$

---

### 3. Computing the Distance Using the Coordinate Formula

The Euclidean distance $d(A, B)$ between two points $A = (x_1, y_1, z_1)$ and $B = (x_2, y_2, z_2)$ in three-dimensional space is given by:

$$
d(A, B) = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2 + (z_2 - z_1)^2}
$$

Substituting $A = (1, 2, 3)$ and $B = (4, -2, 6)$ directly into the formula:

$$
d(A, B) = \sqrt{(4 - 1)^2 + (-2 - 2)^2 + (6 - 3)^2} = \sqrt{3^2 + (-4)^2 + 3^2} = \sqrt{9 + 16 + 9} = \sqrt{34}
$$

---

### 4. Why Both Calculations Give the Same Result

Both calculations produce $\sqrt{34}$ because the coordinate distance formula is **algebraically identical** to taking the norm of the displacement vector $\overrightarrow{AB}$.

- Constructing $\overrightarrow{AB} = (x_2 - x_1, y_2 - y_1, z_2 - z_1)$ computes the signed change in position along each coordinate axis.
- Taking the norm $\|\overrightarrow{AB}\|$ applies the three-dimensional Pythagorean theorem to those coordinate differences.

Geometrically, the straight-line distance between two points $A$ and $B$ is precisely the magnitude of the displacement vector that carries a point from $A$ to $B$.