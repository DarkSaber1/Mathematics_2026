# Exercise 8 – Inverse of a Transformation

## Problem Statement

The matrix

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & \frac12
\end{pmatrix}
$$

describes a scaling of the plane. Find $S^{-1}$ and explain geometrically what the inverse transformation does. Check the action of the pair $S,S^{-1}$ on one simple vector.

## Solution

### 1. Calculation of the Inverse Matrix $S^{-1}$

For a diagonal matrix, the determinant is the product of its diagonal entries:

$$
\det(S) = (2)\left(\frac{1}{2}\right) - (0)(0) = 1
$$

Using the $2 \times 2$ inverse formula:

$$
S^{-1} = \frac{1}{\det(S)} \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 2 \end{pmatrix}
$$

### 2. Geometric Explanation of the Inverse Transformation

- Matrix $S$ stretches the $x$-axis by a factor of $2$ and compresses the $y$-axis by a factor of $\frac{1}{2}$ (halving it).
- Matrix $S^{-1}$ performs the exact opposite (undoing) operation: it compresses the $x$-axis by a factor of $\frac{1}{2}$ (halving it) and stretches the $y$-axis by a factor of $2$ (doubling it).

Geometrically, applying $S^{-1}$ restores any point or vector transformed by $S$ back to its original coordinates in the 2D plane.

### 3. Action of $S$ and $S^{-1}$ on a Sample Vector

Let us test the pair on the simple vector $v = \begin{pmatrix} 3 \\ 4 \end{pmatrix}$.

- **Applying $S$ to $v$:**

$$
v' = Sv = \begin{pmatrix} 2 & 0 \\ 0 & \frac{1}{2} \end{pmatrix} \begin{pmatrix} 3 \\ 4 \end{pmatrix} = \begin{pmatrix} 2(3) + 0(4) \\ 0(3) + \frac{1}{2}(4) \end{pmatrix} = \begin{pmatrix} 6 \\ 2 \end{pmatrix}
$$

- **Applying $S^{-1}$ to $v'$:**

$$
v'' = S^{-1}v' = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 6 \\ 2 \end{pmatrix} = \begin{pmatrix} \frac{1}{2}(6) + 0(2) \\ 0(6) + 2(2) \end{pmatrix} = \begin{pmatrix} 3 \\ 4 \end{pmatrix} = v
$$

### Verification

We verify algebraically that $S^{-1}S = I$:

$$
S^{-1}S = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 2 & 0 \\ 0 & \frac{1}{2} \end{pmatrix} = \begin{pmatrix} \frac{1}{2}(2)+0 & 0+0 \\ 0+0 & 2\left(\frac{1}{2}\right) \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I
$$

Since $S^{-1}(Sv) = Iv = v$, the inverse matrix $S^{-1} = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 2 \end{pmatrix}$ correctly undoes the scaling transformation.