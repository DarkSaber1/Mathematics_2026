# Exercise 5 – Relative Position of Two Lines

## Problem Statement

Analyze the position of

$$
L_1:(x,y,z)=(1,1,0)+t(1,2,1),
$$

$$
L_2:(x,y,z)=(2,0,1)+s(0,1,-1).
$$

If they intersect, give the intersection point. If not, determine whether they are parallel or skew. Justify the classification.

## Solution

### 1. Checking Parallelism via Direction Vectors

First, we extract the direction vectors of both lines:

$$
v_1 = (1, 2, 1), \qquad v_2 = (0, 1, -1)
$$

Two lines are parallel if and only if their direction vectors are scalar multiples of each other ($v_1 = k v_2$ for some $k \in \mathbb{R}$). Comparing the first components gives $1 = k \cdot 0 = 0$, which is impossible.

Therefore, $v_1$ and $v_2$ are not parallel, so $L_1$ and $L_2$ are **neither parallel nor coincident**. They must either **intersect at a single point** or be **skew**.

---

### 2. Testing for Intersection

To determine whether $L_1$ and $L_2$ intersect, we equate their parametric coordinate expressions using distinct parameters $t$ and $s$:

$$
\begin{cases}
1 + t = 2 \\
1 + 2t = s \\
t = 1 - s
\end{cases}
$$

- **Step 1:** Solve the first equation for $t$:

$$
1 + t = 2 \implies t = 1
$$

- **Step 2:** Substitute $t = 1$ into the second equation to find $s$:

$$
1 + 2(1) = s \implies s = 3
$$

- **Step 3:** Check consistency in the third equation ($t = 1 - s$):

$$
\text{Left-hand side: } t = 1
$$

$$
\text{Right-hand side: } 1 - s = 1 - 3 = -2
$$

Since $1 \neq -2$, the system of equations is **inconsistent**—there is no pair $(t, s)$ that satisfies all three equations simultaneously.

---

### 3. Classification and Justification

- **Classification:** The lines $L_1$ and $L_2$ are **skew lines**.
- **Justification:**
  1. Their direction vectors $v_1 = (1, 2, 1)$ and $v_2 = (0, 1, -1)$ are linearly independent (not scalar multiples), proving the lines do not run in the same direction (not parallel).
  2. The coordinate system equating their points has no common solution ($1 \neq -2$), proving they have no point in common (do not intersect).

In $\mathbb{R}^3$, two lines that neither intersect nor are parallel lie in different parallel planes and are classified as **skew**.