# Exercise 12 – Recognizing a Surface from Cross-Sections

## Problem Statement

A certain surface has the following properties:
- the cross-section $z=0$ is a point,
- for $z>0$, the cross-sections $z=\mathrm{const}$ are circles with increasing radius,
- vertical cross-sections through the $Oz$ axis are parabolas.

Propose a simple equation for such a surface and justify your choice.

## Solution

### 1. Proposed Equation

A simple equation for a surface satisfying all three geometric properties is the canonical **circular paraboloid**:

$$
z = x^2 + y^2
$$

*(More generally, any scaled equation $z = a(x^2 + y^2)$ with $a > 0$ also satisfies these conditions; setting $a = 1$ gives the simplest canonical form.)*

---

### 2. Step-by-Step Verification and Justification

We verify that $z = x^2 + y^2$ satisfies each required cross-section property:

1. **Cross-section at $z = 0$ is a single point:**  
   Substituting $z = 0$ into $z = x^2 + y^2$ gives:

$$
x^2 + y^2 = 0
$$

   Since $x^2 \ge 0$ and $y^2 \ge 0$ for all real $(x, y)$, the only real solution is $x = 0$ and $y = 0$. Thus, the slice $z = 0$ consists solely of the single origin point $(0, 0, 0)$.

2. **Horizontal cross-sections $z = c$ for $z > 0$ are circles with increasing radius:**  
   Intersecting the surface with any horizontal plane $z = c$ where $c > 0$ yields:

$$
x^2 + y^2 = c
$$

   This is the equation of a **circle** centered on the $z$-axis at $(0, 0, c)$ with radius:

$$
r(c) = \sqrt{c}
$$

   Because $\sqrt{c}$ is a strictly increasing function for $c > 0$, the circular cross-sections grow wider continuously as $c$ increases. *(Furthermore, for $z < 0$, $x^2 + y^2 = c < 0$ has no real solutions, so the surface lies entirely in the upper half-space $z \ge 0$.)*

3. **Vertical cross-sections through the $Oz$-axis are parabolas:**  
   Any vertical plane containing the $Oz$-axis has the form $ax + by = 0$ (or in cylindrical angle $\theta$, $x = t\cos\theta$ and $y = t\sin\theta$, where $t \in \mathbb{R}$ measures signed horizontal distance from the $z$-axis). Substituting these into $z = x^2 + y^2$ gives:

$$
z = (t\cos\theta)^2 + (t\sin\theta)^2 = t^2(\cos^2\theta + \sin^2\theta) = t^2
$$

   In particular, in the coordinate planes $y = 0$ and $x = 0$, we obtain $z = x^2$ and $z = y^2$. Every vertical slice through the $Oz$-axis is an identical upward-opening **parabola** $z = t^2$ with vertex at $(0, 0, 0)$.