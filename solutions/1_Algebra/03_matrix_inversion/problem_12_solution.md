# Exercise 12 – Parametric Inverse Matrix

## Problem Statement

Consider the matrix containing a parameter $k$:

$$
A(k) =
\begin{pmatrix}
1 & k \\
k & 4
\end{pmatrix}
$$

1. Determine for which values of $k$ the matrix $A(k)$ is singular (not invertible).
2. For all values of $k$ where $A(k)$ is invertible, compute $A^{-1}(k)$.
3. Verify the result by matrix multiplication.

## Solution

### 1. Determining Singularity (Values of $k$)

A square matrix is singular if and only if its determinant is zero ($\det(A) = 0$).

$$
\det(A(k)) = (1)(4) - (k)(k) = 4 - k^2
$$

Setting the determinant to zero:

$$
4 - k^2 = 0 \implies k^2 = 4 \implies k = \pm 2
$$

- For $k = 2$ or $k = -2$, $\det(A(k)) = 0$, so **$A(k)$ is singular (not invertible)**.
- For $k \neq \pm 2$, $\det(A(k)) \neq 0$, so **$A(k)$ is invertible**.

---

### 2. Computing the Parametric Inverse Matrix $A^{-1}(k)$

For $k \neq \pm 2$, we apply the $2 \times 2$ matrix inverse formula:

$$
A^{-1} = \frac{1}{\det(A)} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}
$$

Substituting $a=1$, $b=k$, $c=k$, $d=4$, and $\det(A(k)) = 4 - k^2$:

$$
A^{-1}(k) = \frac{1}{4 - k^2} \begin{pmatrix} 4 & -k \\ -k & 1 \end{pmatrix}
$$

---

### 3. Verification by Matrix Multiplication

We verify that $A(k) A^{-1}(k) = I$ for $k \neq \pm 2$:

$$
A(k) A^{-1}(k) = \begin{pmatrix} 1 & k \\ k & 4 \end{pmatrix} \left[ \frac{1}{4 - k^2} \begin{pmatrix} 4 & -k \\ -k & 1 \end{pmatrix} \right]
$$

Factoring out the scalar $\frac{1}{4 - k^2}$:

$$
A(k) A^{-1}(k) = \frac{1}{4 - k^2} \begin{pmatrix} 1(4) + k(-k) & 1(-k) + k(1) \\ k(4) + 4(-k) & k(-k) + 4(1) \end{pmatrix}
$$

$$
A(k) A^{-1}(k) = \frac{1}{4 - k^2} \begin{pmatrix} 4 - k^2 & -k + k \\ 4k - 4k & 4 - k^2 \end{pmatrix}
$$

$$
A(k) A^{-1}(k) = \frac{1}{4 - k^2} \begin{pmatrix} 4 - k^2 & 0 \\ 0 & 4 - k^2 \end{pmatrix}
$$

$$
A(k) A^{-1}(k) = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I_2
$$

Since $A(k) A^{-1}(k) = I_2$, the inverse matrix formula is verified.