# Exercise 8 – Intersection Point of a Line and a Plane

## Problem Statement

Find the intersection point of

$$
(x,y,z)=(1,0,2)+t(1,2,-1)
$$

with the plane $x+y+z=4$. Check the result by substituting it into both descriptions.

## Solution

### 1. Finding the Parameter $t$ at the Intersection Point

First, we write the coordinates of an arbitrary point on the line in scalar parametric form:

$$
\begin{cases}
x = 1 + t \\
y = 2t \\
z = 2 - t
\end{cases}
\qquad (t \in \mathbb{R})
$$

To find the intersection point with the plane $x + y + z = 4$, we substitute these parametric expressions for $x$, $y$, and $z$ into the plane equation:

$$
(1 + t) + (2t) + (2 - t) = 4
$$

Combine like terms on the left-hand side:

$$
(1 + 2) + (t + 2t - t) = 4 \implies 3 + 2t = 4
$$

Solve for $t$:

$$
2t = 1 \implies t = \frac{1}{2}
$$

---

### 2. Computing the Coordinates of the Intersection Point

Substitute $t = \frac{1}{2}$ back into the parametric equation of the line to find the intersection point $P$:

$$
P = (1, 0, 2) + \frac{1}{2}(1, 2, -1) = \left( 1 + \frac{1}{2},\, 0 + 1,\, 2 - \frac{1}{2} \right) = \left( \frac{3}{2},\, 1,\, \frac{3}{2} \right)
$$

Thus, the unique intersection point is:

$$
P = \left( \frac{3}{2},\, 1,\, \frac{3}{2} \right)
$$

---

### 3. Checking the Result in Both Descriptions

- **Verification in the Plane Equation ($x + y + z = 4$):**  
  Substitute $x = \frac{3}{2}$, $y = 1$, and $z = \frac{3}{2}$:

$$
\frac{3}{2} + 1 + \frac{3}{2} = \frac{6}{2} + 1 = 3 + 1 = 4 \quad (\text{True})
$$

- **Verification in the Parametric Line Equation:**  
  Confirm that a single parameter value $t$ produces all three coordinates of $P$:
  - $x$-coordinate: $1 + t = \frac{3}{2} \implies t = \frac{1}{2}$
  - $y$-coordinate: $0 + 2t = 1 \implies t = \frac{1}{2}$
  - $z$-coordinate: $2 - t = \frac{3}{2} \implies t = \frac{1}{2}$

Since $P = \left( \frac{3}{2}, 1, \frac{3}{2} \right)$ satisfies both the line and plane equations simultaneously, the intersection point is verified.