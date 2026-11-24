# Exercise 14 – Contrast: Intersection and Parallelism

## Problem Statement

From the point $P=(0,0,1)$, two lines are drawn with direction vectors

$$
v_1=(2,1,-1),\qquad v_2=(2,1,0).
$$

For each line, analyze its position relative to the plane $z=0$.

For the line that intersects the plane, find the intersection point. For the other line, explain how you can recognize parallelism without solving an equation.

## Solution

### 1. Geometric Setup: Parametric Lines and Plane Normal

Both lines pass through the initial point $P = (0, 0, 1)$:

- **Line 1 ($L_1$):**

$$
L_1 : (x, y, z) = (0, 0, 1) + t(2, 1, -1) = (2t,\, t,\, 1 - t) \qquad (t \in \mathbb{R})
$$

- **Line 2 ($L_2$):**

$$
L_2 : (x, y, z) = (0, 0, 1) + s(2, 1, 0) = (2s,\, s,\, 1) \qquad (s \in \mathbb{R})
$$

The target plane is the $xy$-coordinate plane $\Pi : z = 0$ (written as $0x + 0y + 1z = 0$), whose unit normal vector points strictly along the vertical $z$-axis:

$$
n = (0, 0, 1)
$$

---

### 2. Analyzing Line 1 ($L_1$) and Finding Its Intersection Point

First, test the orientation of $v_1 = (2, 1, -1)$ relative to $n = (0, 0, 1)$ using the dot product:

$$
v_1 \cdot n = (2)(0) + (1)(0) + (-1)(1) = -1 \neq 0
$$

Because $v_1 \cdot n \neq 0$, $L_1$ is **not parallel** to the plane $z = 0$ and therefore **intersects it at a single unique point**.

To find the intersection point, substitute the $z$-coordinate of $L_1$ ($z = 1 - t$) into the plane equation $z = 0$:

$$
1 - t = 0 \implies t = 1
$$

Substitute $t = 1$ back into the parametric equation of $L_1$:

$$
Q = (0, 0, 1) + 1(2, 1, -1) = (2, 1, 0)
$$

**Verification:** For $Q = (2, 1, 0)$, the third coordinate is $z = 0$ (so $Q$ lies on $\Pi$), and $t = 1$ yields $(2, 1, 0)$ on $L_1$. Thus, the unique intersection point is:

$$
Q = (2, 1, 0)
$$

---

### 3. Analyzing Line 2 ($L_2$) and Recognizing Parallelism Without Solving an Equation

For $L_2$, the direction vector is $v_2 = (2, 1, 0)$. Computing the dot product with the plane normal $n = (0, 0, 1)$ gives:

$$
v_2 \cdot n = (2)(0) + (1)(0) + (0)(1) = 0
$$

Furthermore, the starting point $P = (0, 0, 1)$ has $z = 1 \neq 0$, so $P$ does not lie in the plane $z = 0$. Thus, $L_2$ is **strictly parallel** to the plane $z = 0$ and has **no intersection points** with it.

**How to Recognize Parallelism Without Solving an Equation:**
- **Zero Vertical Rate of Change:** The third component of $v_2 = (2, 1, 0)$ is $0$. Because $z = 0$ is a horizontal plane, moving along $v_2$ changes only the $x$ and $y$ coordinates while keeping the height $z$ completely constant.
- **Constant Non-Zero Elevation:** Since the line starts at $P = (0, 0, 1)$ at height $z = 1$ and never moves up or down, every point on $L_2$ remains permanently at height $z = 1$, hovering $1$ unit above the plane $z = 0$ without ever meeting it.