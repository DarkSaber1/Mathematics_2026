# Exercise 11 – Two Similar Surfaces

## Problem Statement

Compare

$$
x^2+y^2-z^2=1
$$

and

$$
x^2+y^2-z^2=-1.
$$

For several values $z=c$, check whether the cross-section exists and what its radius is. Based on this, describe qualitatively the difference between the surfaces and make sketches.

## Solution

### 1. First Surface: $x^2 + y^2 - z^2 = 1$ (Hyperboloid of One Sheet)

Rewriting the equation for a fixed horizontal plane $z = c$ gives:

$$
x^2 + y^2 = 1 + c^2
$$

Since $c^2 \ge 0$ for every real number $c \in \mathbb{R}$, the right-hand side $1 + c^2$ is **always strictly positive** ($1 + c^2 \ge 1 > 0$). Therefore, a circular cross-section centered at $(0, 0, c)$ exists for **every height $z = c$**, with radius:

$$
r_1(c) = \sqrt{1 + c^2}
$$

Evaluating for several representative values of $z = c$:

| Height $z = c$ | Equation of Cross-Section | Exists? | Radius $r_1(c) = \sqrt{1 + c^2}$ |
| :--- | :--- | :--- | :--- |
| $c = 0$ | $x^2 + y^2 = 1$ | Yes (minimum waist) | $r = \sqrt{1} = 1$ |
| $c = \pm 1$ | $x^2 + y^2 = 2$ | Yes | $r = \sqrt{2} \approx 1.41$ |
| $c = \pm 2$ | $x^2 + y^2 = 5$ | Yes | $r = \sqrt{5} \approx 2.24$ |
| $c = \pm 3$ | $x^2 + y^2 = 10$ | Yes | $r = \sqrt{10} \approx 3.16$ |

- **Qualitative Shape & Sketch Description:**  
  Because cross-sections exist at all heights without interruption, the surface is a **single connected, continuous tube** symmetric around the $z$-axis (a **hyperboloid of one sheet**). It narrows to a minimum circular "waist" of radius $r = 1$ in the plane $z = 0$ and flares outward smoothly both upward ($z \to +\infty$) and downward ($z \to -\infty$), with vertical cross-sections $x = 0$ ($y^2 - z^2 = 1$) and $y = 0$ ($x^2 - z^2 = 1$) forming left-and-right opening hyperbolas.

---

### 2. Second Surface: $x^2 + y^2 - z^2 = -1$ (Hyperboloid of Two Sheets)

Rewriting the equation for a fixed horizontal plane $z = c$ gives:

$$
x^2 + y^2 = c^2 - 1
$$

Because $x^2 + y^2 \ge 0$, real solutions exist **if and only if** $c^2 - 1 \ge 0$, which requires $|c| \ge 1$ (i.e., $c \le -1$ or $c \ge 1$). When $|c| > 1$, the cross-section is a circle centered at $(0, 0, c)$ with radius:

$$
r_2(c) = \sqrt{c^2 - 1}
$$

Evaluating for several representative values of $z = c$:

| Height $z = c$ | Equation of Cross-Section | Exists? | Radius $r_2(c) = \sqrt{c^2 - 1}$ |
| :--- | :--- | :--- | :--- |
| $c = 0$ | $x^2 + y^2 = -1$ | **No** (empty) | — |
| $c = \pm 0.5$ | $x^2 + y^2 = -0.75$ | **No** (empty) | — |
| $c = \pm 1$ | $x^2 + y^2 = 0$ | Yes (degenerate point) | $r = 0$ (vertices $(0, 0, \pm 1)$) |
| $c = \pm 2$ | $x^2 + y^2 = 3$ | Yes | $r = \sqrt{3} \approx 1.73$ |
| $c = \pm 3$ | $x^2 + y^2 = 8$ | Yes | $r = \sqrt{8} = 2\sqrt{2} \approx 2.83$ |

- **Qualitative Shape & Sketch Description:**  
  Because there are no real points in the horizontal slab $-1 < z < 1$, the surface is split into **two completely disconnected pieces** symmetric around the $z$-axis (a **hyperboloid of two sheets**):
- An **upper bowl** starting at its lowest vertex $(0, 0, 1)$ and opening upward for $z \ge 1$ with circular cross-sections of growing radius $\sqrt{z^2 - 1}$.
- A **lower inverted bowl** starting at its highest vertex $(0, 0, -1)$ and opening downward for $z \le -1$ with identical circular cross-sections.
- Vertical cross-sections $x = 0$ ($z^2 - y^2 = 1$) and $y = 0$ ($z^2 - x^2 = 1$) form upward-and-downward opening hyperbolas with vertices at $(0, 0, \pm 1)$.

---

### 3. Core Qualitative Difference

Changing the right-hand side from $+1$ to $-1$ changes the topology of the surface from **one connected sheet** to **two disconnected sheets**:
- In $x^2 + y^2 - z^2 = 1$, the horizontal terms dominate at $z = 0$, wrapping around the $z$-axis with a circular waist of radius $1$ and connecting the upper and lower halves into a single continuous surface.
- In $x^2 + y^2 - z^2 = -1$, the $-z^2$ term dominates near $z = 0$, creating a forbidden gap $-1 < z < 1$ that pinches the waist past zero and separates the surface into two disjoint cups opening in opposite directions along the $z$-axis.