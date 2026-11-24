# Exercise 15 – Complete Classification of a Line Relative to a Plane

## Problem Statement

Let

$$
L:p+tv,\qquad \Pi:n\cdot x=d.
$$

State the conditions distinguishing the three cases: one intersection point, parallel with no common points, and the line contained in the plane. Then illustrate each case with your own simple numerical example.

## Solution

### 1. Mathematical Criterion Classifying the Relative Position of $L$ and $\Pi$

To analyze where the line $L : x = p + tv$ ($t \in \mathbb{R}$, with $v \neq \mathbf{0}$) meets the plane $\Pi : n \cdot x = d$ ($n \neq \mathbf{0}$), we substitute $x = p + tv$ into the plane equation[cite: 3]:

$$
n \cdot (p + tv) = d \implies (n \cdot v)\,t = d - (n \cdot p)
$$

This linear equation in $t$ partitions the geometric relationship between $L$ and $\Pi$ into three mutually exclusive cases:

1. **Case 1: One Unique Intersection Point**
   - **Condition:**

$$
n \cdot v \neq 0
$$

   - **Explanation:** The line's direction vector $v$ is not perpendicular to the plane's normal vector $n$, meaning the line approaches the plane obliquely and pierces it at a single unique parameter value:

$$
t = \frac{d - n \cdot p}{n \cdot v}
$$

2. **Case 2: Parallel with No Common Points (Strictly Parallel)**
   - **Condition:**

$$
n \cdot v = 0 \qquad \text{and} \qquad n \cdot p \neq d
$$

   - **Explanation:** Since $n \cdot v = 0$, the line moves strictly perpendicular to the normal vector $n$ (parallel to $\Pi$). However, because its base point $p$ does not satisfy the plane equation ($n \cdot p \neq d$), the equation $0 \cdot t = d - n \cdot p \neq 0$ has no solution, and the line remains at a constant non-zero distance from the plane.

3. **Case 3: Line Contained in the Plane ($L \subset \Pi$)**
   - **Condition:**

$$
n \cdot v = 0 \qquad \text{and} \qquad n \cdot p = d
$$

   - **Explanation:** The line moves parallel to the plane ($n \cdot v = 0$) and its base point $p$ lies directly on the plane ($n \cdot p = d$). The equation reduces to $0 \cdot t = 0$, which holds for every $t \in \mathbb{R}$, meaning infinitely many points (the entire line) lie inside $\Pi$.

---

### 2. Numerical Examples Illustrating Each Case

In all three examples below, let the plane be the horizontal $xy$-plane $\Pi : z = 0$, so that:

$$
n = (0, 0, 1), \qquad d = 0
$$

- **Example for Case 1 (One Intersection Point):**  
  Let $p = (0, 0, 2)$ and $v = (1, 0, -1)$, giving $L_1 : (x, y, z) = (0, 0, 2) + t(1, 0, -1)$.
  - **Check conditions:**

$$
n \cdot v = (0)(1) + (0)(0) + (1)(-1) = -1 \neq 0
$$

  - **Result:** Solving $2 - t = 0$ gives $t = 2$, so $L_1$ intersects $\Pi$ at the single point $(2, 0, 0)$.

- **Example for Case 2 (Parallel with No Common Points):**  
  Let $p = (0, 0, 2)$ and $v = (1, 1, 0)$, giving $L_2 : (x, y, z) = (0, 0, 2) + t(1, 1, 0)$.
  - **Check conditions:**

$$
n \cdot v = (0)(1) + (0)(1) + (1)(0) = 0, \qquad n \cdot p = (0)(0) + (0)(0) + (1)(2) = 2 \neq 0
$$

  - **Result:** The line stays permanently at height $z = 2$, strictly parallel to $\Pi : z = 0$ with zero intersection points.

- **Example for Case 3 (Line Contained in the Plane):**  
  Let $p = (1, 2, 0)$ and $v = (1, 1, 0)$, giving $L_3 : (x, y, z) = (1, 2, 0) + t(1, 1, 0)$.
  - **Check conditions:**

$$
n \cdot v = (0)(1) + (0)(1) + (1)(0) = 0, \qquad n \cdot p = (0)(1) + (0)(2) + (1)(0) = 0 = d
$$

  - **Result:** Every point $(1 + t,\, 2 + t,\, 0)$ satisfies $z = 0$, confirming that $L_3$ lies completely inside $\Pi$.