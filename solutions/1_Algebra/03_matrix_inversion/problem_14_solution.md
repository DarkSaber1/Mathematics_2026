# Exercise 14 – Block Diagonal Matrix Inverse

## Problem Statement

Consider the block matrix

$$
M=
\begin{pmatrix}
A & 0 \\
0 & B
\end{pmatrix}
$$

where $A$ and $B$ are invertible square matrices (not necessarily of the same size) and $0$ denotes zero blocks of appropriate sizes.

1. Show that $M$ is invertible and that its inverse is given by

$$
M^{-1}=
\begin{pmatrix}
A^{-1} & 0 \\
0 & B^{-1}
\end{pmatrix}
$$

2. Apply this result to find the inverse of

$$
M=
\begin{pmatrix}
1 & 2 & 0 & 0 \\
3 & 4 & 0 & 0 \\
0 & 0 & 5 & 6 \\
0 & 0 & 7 & 8
\end{pmatrix}
$$

## Solution

### 1. Proof of the Block Diagonal Inverse Formula

To show that $M^{-1} = \begin{pmatrix} A^{-1} & 0 \\ 0 & B^{-1} \end{pmatrix}$, we compute the block matrix product $M M^{-1}$ using standard block multiplication rules:

$$
M M^{-1} = \begin{pmatrix} A & 0 \\ 0 & B \end{pmatrix} \begin{pmatrix} A^{-1} & 0 \\ 0 & B^{-1} \end{pmatrix}
$$

Multiplying block-by-block:

$$
M M^{-1} = \begin{pmatrix} A A^{-1} + 0 \cdot 0 & A \cdot 0 + 0 \cdot B^{-1} \\ 0 \cdot A^{-1} + B \cdot 0 & 0 \cdot 0 + B B^{-1} \end{pmatrix}
$$

$$
M M^{-1} = \begin{pmatrix} A A^{-1} & 0 \\ 0 & B B^{-1} \end{pmatrix}
$$

Since $A$ and $B$ are invertible matrices, $A A^{-1} = I_k$ and $B B^{-1} = I_m$ (where $k$ and $m$ are the dimensions of $A$ and $B$ respectively):

$$
M M^{-1} = \begin{pmatrix} I_k & 0 \\ 0 & I_m \end{pmatrix} = I_{k+m}
$$

Similarly, checking $M^{-1} M$:

$$
M^{-1} M = \begin{pmatrix} A^{-1} & 0 \\ 0 & B^{-1} \end{pmatrix} \begin{pmatrix} A & 0 \\ 0 & B \end{pmatrix} = \begin{pmatrix} A^{-1}A & 0 \\ 0 & B^{-1}B \end{pmatrix} = \begin{pmatrix} I_k & 0 \\ 0 & I_m \end{pmatrix} = I_{k+m}
$$

This proves that $M^{-1} = \begin{pmatrix} A^{-1} & 0 \\ 0 & B^{-1} \end{pmatrix}$.

---

### 2. Computing the Inverse of the Given $4 \times 4$ Matrix

The matrix $M$ can be partitioned into $2 \times 2$ diagonal blocks:

$$
M = \begin{pmatrix} A & 0 \\ 0 & B \end{pmatrix}
$$

where

$$
A = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix},\qquad B = \begin{pmatrix} 5 & 6 \\ 7 & 8 \end{pmatrix}
$$

- **Inverting Block $A$:**

$$
\det(A) = (1)(4) - (2)(3) = 4 - 6 = -2
$$

$$
A^{-1} = \frac{1}{-2} \begin{pmatrix} 4 & -2 \\ -3 & 1 \end{pmatrix} = \begin{pmatrix} -2 & 1 \\ \frac{3}{2} & -\frac{1}{2} \end{pmatrix}
$$

- **Inverting Block $B$:**

$$
\det(B) = (5)(8) - (6)(7) = 40 - 42 = -2
$$

$$
B^{-1} = \frac{1}{-2} \begin{pmatrix} 8 & -6 \\ -7 & 5 \end{pmatrix} = \begin{pmatrix} -4 & 3 \\ \frac{7}{2} & -\frac{5}{2} \end{pmatrix}
$$

Combining $A^{-1}$ and $B^{-1}$ into $M^{-1}$:

$$
M^{-1} = \begin{pmatrix} -2 & 1 & 0 & 0 \\ \frac{3}{2} & -\frac{1}{2} & 0 & 0 \\ 0 & 0 & -4 & 3 \\ 0 & 0 & \frac{7}{2} & -\frac{5}{2} \end{pmatrix}
$$

---

### Verification

We multiply $M M^{-1}$ to confirm the result:

- **Top-left $2 \times 2$ block:**

$$
\begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix} \begin{pmatrix} -2 & 1 \\ \frac{3}{2} & -\frac{1}{2} \end{pmatrix} = \begin{pmatrix} -2 + 3 & 1 - 1 \\ -6 + 6 & 3 - 2 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}
$$

- **Bottom-right $2 \times 2$ block:**

$$
\begin{pmatrix} 5 & 6 \\ 7 & 8 \end{pmatrix} \begin{pmatrix} -4 & 3 \\ \frac{7}{2} & -\frac{5}{2} \end{pmatrix} = \begin{pmatrix} -20 + 21 & 15 - 15 \\ -28 + 28 & 21 - 20 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}
$$

- **Off-diagonal $2 \times 2$ blocks:** Yield zero matrices of size $2 \times 2$.

$$
M M^{-1} = \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix} = I_4
$$

Since $M M^{-1} = I_4$, the block matrix inverse is verified.