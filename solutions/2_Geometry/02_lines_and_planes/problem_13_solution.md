# Exercise 13 – Closest Point on a Plane

## Problem Statement

Find the point on the plane $x+2y+2z=4$ closest to $P=(3,0,0)$. Give the distance and check that the segment joining the two points is perpendicular to the plane.

## Solution

### 1. Finding the Closest Point $Q$ on the Plane

From the equation of the plane $\Pi : x + 2y + 2z = 4$, we identify its normal vector:

$$
n = (1, 2, 2)
$$

Geometrically, the point $Q$ on $\Pi$ closest to $P = (3, 0, 0)$ is the orthogonal projection of $P$ onto $\Pi$, which is the intersection of $\Pi$ with the line $L$ passing through $P$ in the direction of $n$. The parametric equation of $L$ is:

$$
L : (x, y, z) = (3, 0, 0) + t(1, 2, 2) \implies \begin{cases} x = 3 + t \\ y = 2t \\ z = 2t \end{cases}
$$

Substitute these parametric coordinates into the plane equation $x + 2y + 2z = 4$:

$$
(3 + t) + 2(2t) + 2(2t) = 4
$$

$$
3 + t + 4t + 4t = 4 \implies 3 + 9t = 4 \implies 9t = 1 \implies t = \frac{1}{9}
$$

Substitute $t = \frac{1}{9}$ back into the parametric equation of $L$ to obtain the coordinates of the closest point $Q$:

$$
Q = (3, 0, 0) + \frac{1}{9}(1, 2, 2) = \left( 3 + \frac{1}{9},\, \frac{2}{9},\, \frac{2}{9} \right) = \left( \frac{28}{9},\, \frac{2}{9},\, \frac{2}{9} \right)
$$

Thus, the point on the plane closest to $P$ is:

$$
Q = \left( \frac{28}{9},\, \frac{2}{9},\, \frac{2}{9} \right)
$$

---

### 2. Computing the Distance Between $P$ and the Plane

- **Method 1: Length of the Displacement Vector $\overrightarrow{QP}$:**  
  First, construct the vector connecting $Q$ to $P$:

$$
\overrightarrow{QP} = P - Q = (3, 0, 0) - \left( \frac{28}{9},\, \frac{2}{9},\, \frac{2}{9} \right) = \left( -\frac{1}{9},\, -\frac{2}{9},\, -\frac{2}{9} \right)
$$

  Compute its Euclidean norm $\|\overrightarrow{QP}\|$:

$$
d = \|\overrightarrow{QP}\| = \sqrt{\left(-\frac{1}{9}\right)^2 + \left(-\frac{2}{9}\right)^2 + \left(-\frac{2}{9}\right)^2} = \sqrt{\frac{1 + 4 + 4}{81}} = \sqrt{\frac{9}{81}} = \frac{3}{9} = \frac{1}{3}
$$

- **Method 2: Verification via the Point-to-Plane Distance Formula:**

$$
d(P, \Pi) = \frac{|1(3) + 2(0) + 2(0) - 4|}{\sqrt{1^2 + 2^2 + 2^2}} = \frac{|3 - 4|}{\sqrt{1 + 4 + 4}} = \frac{|-1|}{\sqrt{9}} = \frac{1}{3}
$$

Both methods confirm the distance is $\frac{1}{3}$.

---

### 3. Checking That the Segment $PQ$ Is Perpendicular to the Plane

A line segment $PQ$ is perpendicular to the plane $\Pi$ if and only if its direction vector $\overrightarrow{QP}$ is parallel to (a scalar multiple of) the plane's normal vector $n = (1, 2, 2)$:

$$
\overrightarrow{QP} = \left( -\frac{1}{9},\, -\frac{2}{9},\, -\frac{2}{9} \right) = -\frac{1}{9}(1, 2, 2) = -\frac{1}{9} n
$$

Since $\overrightarrow{QP}$ is a non-zero scalar multiple of $n$, it is orthogonal to every vector lying inside the plane $\Pi$, confirming that the segment $PQ$ meets the plane at a $90^\circ$ right angle.