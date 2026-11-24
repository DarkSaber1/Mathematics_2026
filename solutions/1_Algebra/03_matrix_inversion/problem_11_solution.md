# Exercise 11 – Parameter and Invertibility

## Problem Statement

For

$$
A(t)=
\begin{pmatrix}
1 & t \\
t & 1 \\
\end{pmatrix}
$$

find all $t$ for which the matrix is invertible, and then give a formula for $A(t)^{-1}$. Explain what happens to this formula at the excluded values.

## Solution

### 1. Finding Values of $t$ for Which $A(t)$ Is Invertible

A square $2 \times 2$ matrix is invertible if and only if its determinant is non-zero ($\det(A(t)) \neq 0$).

We compute the determinant of $A(t)$:

$$
\det(A(t)) = (1)(1) - (t)(t) = 1 - t^2
$$

Setting the determinant equal to zero to find the singular (non-invertible) cases:

$$
1 - t^2 = 0 \implies t^2 = 1 \implies t = 1 \quad \text{or} \quad t = -1
$$

Therefore, $A(t)$ is invertible for all real numbers $t$ except $t = 1$ and $t = -1$:

$$
t \in \mathbb{R} \setminus \{-1, 1\}
$$

---

### 2. Formula for the Inverse Matrix $A(t)^{-1}$

For any $t \neq \pm 1$, we apply the standard $2 \times 2$ inverse formula:

$$
A(t)^{-1} = \frac{1}{\det(A(t))} \begin{pmatrix} 1 & -t \\ -t & 1 \end{pmatrix}
$$

Substituting $\det(A(t)) = 1 - t^2$:

$$
A(t)^{-1} = \frac{1}{1 - t^2} \begin{pmatrix} 1 & -t \\ -t & 1 \end{pmatrix} = \begin{pmatrix} \frac{1}{1 - t^2} & \frac{-t}{1 - t^2} \\ \frac{-t}{1 - t^2} & \frac{1}{1 - t^2} \end{pmatrix}
$$

---

### 3. Behavior of the Formula at the Excluded Values ($t = \pm 1$)

At the excluded values $t = 1$ and $t = -1$:

- **Division by Zero in the Formula:**  
  The denominator $1 - t^2$ in the scalar factor $\frac{1}{1 - t^2}$ becomes zero ($1 - (\pm 1)^2 = 0$), which makes division undefined. Consequently, every entry of the formula approaches $\pm \infty$ and does not exist as a real number.

- **Structural Matrix Behavior:**
  - When $t = 1$:

$$
A(1) = \begin{pmatrix} 1 & 1 \\ 1 & 1 \end{pmatrix}
$$

    Both rows are identical, meaning the rows are linearly dependent.
  - When $t = -1$:

$$
A(-1) = \begin{pmatrix} 1 & -1 \\ -1 & 1 \end{pmatrix}
$$

    Row 2 is $-1$ times Row 1, again making the rows linearly dependent. In both cases, information is lost (rank drops from $2$ to $1$), so the transformation cannot be reversed.

---

### Verification

For $t \neq \pm 1$, we multiply $A(t) A(t)^{-1}$:

$$
A(t) A(t)^{-1} = \begin{pmatrix} 1 & t \\ t & 1 \end{pmatrix} \left[ \frac{1}{1 - t^2} \begin{pmatrix} 1 & -t \\ -t & 1 \end{pmatrix} \right] = \frac{1}{1 - t^2} \begin{pmatrix} 1 - t^2 & -t + t \\ t - t & -t^2 + 1 \end{pmatrix} = \frac{1}{1 - t^2} \begin{pmatrix} 1 - t^2 & 0 \\ 0 & 1 - t^2 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I_2
$$