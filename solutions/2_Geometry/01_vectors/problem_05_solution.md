# Exercise 5 – Angle Between Vectors

## Problem Statement

Given $u=(1,1,0)$ and $v=(1,0,1)$:

1. Use the sign of $u\cdot v$ to predict the type of angle.
2. Compute the angle.
3. Compare the result with the prediction.

## Solution

### 1. Using the Sign of $u \cdot v$ to Predict the Type of Angle

The geometric dot product formula is $u \cdot v = \|u\|\,\|v\|\cos\theta$, where $\theta \in [0^\circ, 180^\circ]$ is the angle between the two non-zero vectors. Since $\|u\| > 0$ and $\|v\| > 0$, the sign of $\cos\theta$ is determined entirely by the sign of $u \cdot v$:

- $u \cdot v > 0 \implies \cos\theta > 0 \implies \theta$ is **acute** ($0^\circ \le \theta < 90^\circ$).
- $u \cdot v = 0 \implies \cos\theta = 0 \implies \theta$ is **right** ($\theta = 90^\circ$).
- $u \cdot v < 0 \implies \cos\theta < 0 \implies \theta$ is **obtuse** ($90^\circ < \theta \le 180^\circ$).

We compute the dot product of $u = (1, 1, 0)$ and $v = (1, 0, 1)$:

$$
u \cdot v = (1)(1) + (1)(0) + (0)(1) = 1 + 0 + 0 = 1
$$

**Prediction:** Because $u \cdot v = 1 > 0$, we predict that the angle $\theta$ between $u$ and $v$ is **acute** (strictly less than $90^\circ$).

---

### 2. Computing the Exact Angle

Using the cosine formula for the angle between two vectors:

$$
\cos\theta = \frac{u \cdot v}{\|u\|\,\|v\|}
$$

First, compute the Euclidean lengths (norms) of $u$ and $v$:

$$
\|u\| = \sqrt{1^2 + 1^2 + 0^2} = \sqrt{2}
$$

$$
\|v\| = \sqrt{1^2 + 0^2 + 1^2} = \sqrt{2}
$$

Substitute $u \cdot v = 1$, $\|u\| = \sqrt{2}$, and $\|v\| = \sqrt{2}$ into the formula:

$$
\cos\theta = \frac{1}{\sqrt{2} \cdot \sqrt{2}} = \frac{1}{2}
$$

Taking the inverse cosine for $\theta \in [0^\circ, 180^\circ]$:

$$
\theta = \arccos\left(\frac{1}{2}\right) = 60^\circ \quad \left(\text{or } \frac{\pi}{3}\text{ radians}\right)
$$

---

### 3. Comparison with the Prediction

The computed angle $\theta = 60^\circ$ ($\frac{\pi}{3}\text{ rad}$) satisfies $0^\circ < 60^\circ < 90^\circ$, confirming that it is indeed an **acute angle**. This matches our initial qualitative prediction made from the positive sign of the dot product $u \cdot v = 1 > 0$.