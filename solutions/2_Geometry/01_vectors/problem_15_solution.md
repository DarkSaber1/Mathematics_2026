# Exercise 15 – Comparing Directions Using the Cosine of the Angle

## Problem Statement

Given

$$
a=(1,2,1),\qquad b=(2,4,2),\qquad c=(2,0,3).
$$

For each pair, compute

$$
\frac{u\cdot v}{\|u\|\,\|v\|}.
$$

Order the pairs by increasing angle between the vectors. Explain why for $a$ and $b$ the value is $1$ even though the vectors have different lengths.

## Solution

### 1. Computing Vector Lengths (Norms)

First, we compute the Euclidean length (norm) of each vector $a = (1, 2, 1)$, $b = (2, 4, 2)$, and $c = (2, 0, 3)$:

$$
\|a\| = \sqrt{1^2 + 2^2 + 1^2} = \sqrt{1 + 4 + 1} = \sqrt{6}
$$

$$
\|b\| = \sqrt{2^2 + 4^2 + 2^2} = \sqrt{4 + 16 + 4} = \sqrt{24} = 2\sqrt{6}
$$

$$
\|c\| = \sqrt{2^2 + 0^2 + 3^2} = \sqrt{4 + 0 + 9} = \sqrt{13}
$$

---

### 2. Computing $\cos\theta = \frac{u \cdot v}{\|u\|\,\|v\|}$ for Each Pair

There are three distinct pairs among $\{a, b, c\}$:

- **Pair 1: $a$ and $b$**  
  Compute the dot product:

$$
a \cdot b = (1)(2) + (2)(4) + (1)(2) = 2 + 8 + 2 = 12
$$

  Compute the cosine ratio:

$$
\cos\theta_{ab} = \frac{a \cdot b}{\|a\|\,\|b\|} = \frac{12}{\sqrt{6} \cdot 2\sqrt{6}} = \frac{12}{2 \cdot 6} = \frac{12}{12} = 1
$$

- **Pair 2: $a$ and $c$**  
  Compute the dot product:

$$
a \cdot c = (1)(2) + (2)(0) + (1)(3) = 2 + 0 + 3 = 5
$$

  Compute the cosine ratio:

$$
\cos\theta_{ac} = \frac{a \cdot c}{\|a\|\,\|c\|} = \frac{5}{\sqrt{6} \cdot \sqrt{13}} = \frac{5}{\sqrt{78}} \approx 0.5661
$$

- **Pair 3: $b$ and $c$**  
  Compute the dot product:

$$
b \cdot c = (2)(2) + (4)(0) + (2)(3) = 4 + 0 + 6 = 10
$$

  Compute the cosine ratio:

$$
\cos\theta_{bc} = \frac{b \cdot c}{\|b\|\,\|c\|} = \frac{10}{2\sqrt{6} \cdot \sqrt{13}} = \frac{5}{\sqrt{78}} \approx 0.5661
$$

---

### 3. Ordering the Pairs by Increasing Angle

For angles $\theta \in [0^\circ, 180^\circ]$, the cosine function $\cos\theta$ is **strictly decreasing**: a larger cosine value corresponds to a smaller angle.

Comparing our computed cosine values:

$$
1 > \frac{5}{\sqrt{78}} = \frac{5}{\sqrt{78}}
$$

- For $(a, b)$: $\cos\theta_{ab} = 1 \implies \theta_{ab} = \arccos(1) = 0^\circ$.
- For $(a, c)$ and $(b, c)$: $\cos\theta_{ac} = \cos\theta_{bc} = \frac{5}{\sqrt{78}} \implies \theta_{ac} = \theta_{bc} = \arccos\left(\frac{5}{\sqrt{78}}\right) \approx 55.52^\circ$.

Therefore, ordering the pairs by **increasing angle** gives:

1. **Smallest angle ($0^\circ$):** Pair $(a, b)$
2. **Tied for largest angle ($\approx 55.52^\circ$):** Pairs $(a, c)$ and $(b, c)$ have the exact same angle ($\theta_{ac} = \theta_{bc}$).

---

### 4. Explanation of Why $\frac{a \cdot b}{\|a\|\,\|b\|} = 1$ Despite Different Lengths

Notice that $b = (2, 4, 2) = 2(1, 2, 1) = 2a$. Because $b$ is a **positive scalar multiple** of $a$, both vectors point in the **exact same direction and orientation** (so the angle between them is $\theta_{ab} = 0^\circ$, and $\cos 0^\circ = 1$).

Algebraically, the expression $\frac{u \cdot v}{\|u\|\,\|v\|}$ automatically normalizes both vectors into unit vectors before taking their dot product:

$$
\frac{a \cdot b}{\|a\|\,\|b\|} = \left(\frac{a}{\|a\|}\right) \cdot \left(\frac{b}{\|b\|}\right)
$$

Dividing $b$ by $\|b\| = 2\sqrt{6}$ cancels out its extra length factor of $2$, leaving the exact same unit direction vector as $\frac{a}{\|a\|}$:

$$
\frac{a}{\|a\|} = \left(\frac{1}{\sqrt{6}},\, \frac{2}{\sqrt{6}},\, \frac{1}{\sqrt{6}}\right), \qquad \frac{b}{\|b\|} = \left(\frac{2}{2\sqrt{6}},\, \frac{4}{2\sqrt{6}},\, \frac{2}{2\sqrt{6}}\right) = \left(\frac{1}{\sqrt{6}},\, \frac{2}{\sqrt{6}},\, \frac{1}{\sqrt{6}}\right)
$$

Because this normalized dot product depends solely on **direction** and is completely invariant to positive scaling, differing vector lengths have no effect on the resulting value of $1$.