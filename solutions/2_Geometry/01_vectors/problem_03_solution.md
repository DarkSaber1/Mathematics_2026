# Exercise 3 – Vector Normalization

## Problem Statement

For $v=(3,4)$ find a unit vector $e$ with the same direction and orientation. Check that $\|e\|=1$, reconstruct $v$ in the form $v=\|v\|e$, and explain what changes during normalization and what remains unchanged.

## Solution

### 1. Finding the Unit Vector $e$

To normalize a non-zero vector $v = (3, 4)$ into a unit vector $e$ pointing in the same direction and orientation, we divide $v$ by its Euclidean length (norm) $\|v\|$:

$$
e = \frac{1}{\|v\|} v
$$

First, compute the norm of $v = (3, 4)$:

$$
\|v\| = \sqrt{3^2 + 4^2} = \sqrt{9 + 16} = \sqrt{25} = 5
$$

Now multiply $v$ by the positive scalar $\frac{1}{\|v\|} = \frac{1}{5}$:

$$
e = \frac{1}{5} (3, 4) = \left( \frac{3}{5},\, \frac{4}{5} \right)
$$

---

### 2. Checking That $\|e\| = 1$

We verify that $e = \left( \frac{3}{5}, \frac{4}{5} \right)$ is indeed a unit vector by computing its norm:

$$
\|e\| = \sqrt{\left(\frac{3}{5}\right)^2 + \left(\frac{4}{5}\right)^2} = \sqrt{\frac{9}{25} + \frac{16}{25}} = \sqrt{\frac{25}{25}} = \sqrt{1} = 1
$$

Thus, $\|e\| = 1$ is confirmed.

---

### 3. Reconstructing $v$ in the Form $v = \|v\|e$

Using $\|v\| = 5$ and $e = \left( \frac{3}{5}, \frac{4}{5} \right)$, we multiply the scalar norm by the unit direction vector:

$$
\|v\|e = 5 \left( \frac{3}{5},\, \frac{4}{5} \right) = \left( 5 \cdot \frac{3}{5},\, 5 \cdot \frac{4}{5} \right) = (3, 4) = v
$$

This recovers the original vector $v$ exactly.

---

### 4. What Changes and What Remains Unchanged During Normalization

Normalization decomposes a vector into its pure magnitude and pure direction:

- **What Changes:**
  - **Magnitude (Length):** The length of the vector is rescaled from its original value ($\|v\| = 5$) to exactly $1$ ($\|e\| = 1$).
  - **Coordinate Values:** Each component is scaled by the factor $\frac{1}{\|v\|}$ (here, divided by $5$).

- **What Remains Unchanged:**
  - **Direction (Line of Action):** Because $e$ is a scalar multiple of $v$, both vectors lie along the exact same line through the origin (same slope $\frac{4}{3}$).
  - **Orientation (Sense):** Because the scaling factor $\frac{1}{\|v\|} = \frac{1}{5} > 0$ is strictly positive, the vector continues to point in the exact same sense (into the first quadrant), rather than flipping to the opposite side.