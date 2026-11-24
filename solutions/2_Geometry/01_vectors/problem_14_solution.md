# Exercise 14 – Closest Point on a Line

## Problem Statement

Given a point $P=(4,1)$ and a line through the origin with direction $v=(1,2)$. Using projection, find the closest point on the line, the distance from $P$ to the line, and verify that the appropriate vector is perpendicular to the direction of the line.

## Solution

### 1. Finding the Closest Point on the Line Using Projection

Let $O = (0, 0)$ denote the origin, and let $p = \overrightarrow{OP} = (4, 1)$ be the position vector of point $P$. Because the line passes through the origin with direction vector $v = (1, 2)$, every point on the line is a scalar multiple of $v$.

Geometrically, the closest point $Q$ on the line to $P$ is the foot of the perpendicular dropped from $P$ onto the line, whose position vector $q = \overrightarrow{OQ}$ is the orthogonal projection of $p$ onto $v$:

$$
q = \mathrm{proj}_v\,p = \frac{p \cdot v}{v \cdot v} v
$$

First, compute the required dot products:

$$
p \cdot v = (4)(1) + (1)(2) = 4 + 2 = 6
$$

$$
v \cdot v = (1)(1) + (2)(2) = 1 + 4 = 5
$$

Substituting these into the projection formula gives the position vector of the closest point $Q$:

$$
q = \frac{6}{5}(1, 2) = \left( \frac{6}{5},\, \frac{12}{5} \right)
$$

Thus, the closest point on the line to $P$ is:

$$
Q = \left( \frac{6}{5},\, \frac{12}{5} \right)
$$

---

### 2. Computing the Distance from $P$ to the Line

The shortest distance $d$ from $P = (4, 1)$ to the line is the Euclidean length (norm) of the perpendicular displacement vector $\overrightarrow{QP} = p - q$:

$$
\overrightarrow{QP} = p - q = (4, 1) - \left( \frac{6}{5},\, \frac{12}{5} \right) = \left( \frac{20}{5} - \frac{6}{5},\, \frac{5}{5} - \frac{12}{5} \right) = \left( \frac{14}{5},\, -\frac{7}{5} \right)
$$

Computing the length $\|\overrightarrow{QP}\|$:

$$
d = \|\overrightarrow{QP}\| = \sqrt{\left(\frac{14}{5}\right)^2 + \left(-\frac{7}{5}\right)^2} = \sqrt{\frac{196}{25} + \frac{49}{25}} = \sqrt{\frac{245}{25}} = \frac{\sqrt{49 \cdot 5}}{5} = \frac{7\sqrt{5}}{5}
$$

---

### 3. Verifying Perpendicularity to the Direction of the Line

For $Q$ to truly be the closest point on the line, the error/residual vector $\overrightarrow{QP} = \left( \frac{14}{5}, -\frac{7}{5} \right)$ connecting the line to $P$ must be perpendicular (orthogonal) to the line's direction vector $v = (1, 2)$.

We verify this by computing their dot product:

$$
\overrightarrow{QP} \cdot v = \left(\frac{14}{5}\right)(1) + \left(-\frac{7}{5}\right)(2) = \frac{14}{5} - \frac{14}{5} = 0
$$

Since $\overrightarrow{QP} \cdot v = 0$, the segment $QP$ forms a $90^\circ$ right angle with the line, confirming that $Q = \left( \frac{6}{5}, \frac{12}{5} \right)$ is the unique point on the line minimizing the distance to $P$.