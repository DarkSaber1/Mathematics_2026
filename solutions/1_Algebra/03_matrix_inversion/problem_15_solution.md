# Exercise 15 – Inverse of a Permutation Matrix

## Problem Statement

Let

$$
P=
\begin{pmatrix}
0 & 1 & 0 \\
0 & 0 & 1 \\
1 & 0 & 0
\end{pmatrix}
$$

1. Compute $P^T$ (the transpose of $P$).
2. Compute $P P^T$ and $P^T P$.
3. What is $P^{-1}$? Explain why $P^{-1} = P^T$ holds for any permutation matrix.

## Solution

### 1. Computation of $P^T$

To find the transpose $P^T$, we swap the rows and columns of $P$:

$$
P^T =
\begin{pmatrix}
0 & 0 & 1 \\
1 & 0 & 0 \\
0 & 1 & 0
\end{pmatrix}
$$

---

### 2. Computing $P P^T$ and $P^T P$

- **First, computing $P P^T$:**

$$
P P^T = \begin{pmatrix} 0 & 1 & 0 \\ 0 & 0 & 1 \\ 1 & 0 & 0 \end{pmatrix} \begin{pmatrix} 0 & 0 & 1 \\ 1 & 0 & 0 \\ 0 & 1 & 0 \end{pmatrix}
$$

- **Row 1:** $(0(0)+1(1)+0(0), \; 0(0)+1(0)+0(1), \; 0(1)+1(0)+0(0)) = (1, 0, 0)$
- **Row 2:** $(0(0)+0(1)+1(0), \; 0(0)+0(0)+1(1), \; 0(1)+0(0)+1(0)) = (0, 1, 0)$
- **Row 3:** $(1(0)+0(1)+0(0), \; 1(0)+0(0)+0(1), \; 1(1)+0(0)+0(0)) = (0, 0, 1)$

$$
P P^T = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix} = I_3
$$

- **Next, computing $P^T P$:**

$$
P^T P = \begin{pmatrix} 0 & 0 & 1 \\ 1 & 0 & 0 \\ 0 & 1 & 0 \end{pmatrix} \begin{pmatrix} 0 & 1 & 0 \\ 0 & 0 & 1 \\ 1 & 0 & 0 \end{pmatrix}
$$

- **Row 1:** $(0(0)+0(0)+1(1), \; 0(1)+0(0)+1(0), \; 0(0)+0(1)+1(0)) = (1, 0, 0)$
- **Row 2:** $(1(0)+0(0)+0(1), \; 1(1)+0(0)+0(0), \; 1(0)+0(1)+0(0)) = (0, 1, 0)$
- **Row 3:** $(0(0)+1(0)+0(1), \; 0(1)+1(0)+0(0), \; 0(0)+1(1)+0(0)) = (0, 0, 1)$

$$
P^T P = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix} = I_3
$$

---

### 3. Determining $P^{-1}$ and General Proof

Since $P P^T = I_3$ and $P^T P = I_3$, the inverse matrix is:

$$
P^{-1} = P^T = \begin{pmatrix} 0 & 0 & 1 \\ 1 & 0 & 0 \\ 0 & 1 & 0 \end{pmatrix}
$$

### Structural and Geometric Explanation

A permutation matrix $P$ is formed by reordering (permuting) the rows of the identity matrix $I$.

1. **Orthonormal Vector Structure:** The rows (and columns) of $P$ form an orthonormal basis. Every row has length $1$, and any two distinct rows are orthogonal (their dot product is zero).
2. **Matrix Product Mechanics:** When computing the $(i, j)$-th entry of $P P^T$, we take the dot product of row $i$ of $P$ and row $j$ of $P$.
   - When $i = j$, the dot product of a unit row vector with itself is $1$.
   - When $i \neq j$, the dot product of two distinct orthogonal row vectors is $0$.
3. **Geometric Reversibility:** Operating $P$ on a vector permutes its components. Transposition $P^T$ moves each entry back to its original row position, effectively reversing the permutation.

Therefore, for any permutation matrix $P$, the identity $P^{-1} = P^T$ always holds.