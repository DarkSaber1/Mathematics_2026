# Exercise 9 – Matrix Equation

## Problem Statement

Given

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix},\qquad B=
\begin{pmatrix}
3 & 1 \\
2 & 4
\end{pmatrix}
$$

Solve the equation $AX=B$ for $X$. Before calculating, decide on which side of the equation $A^{-1}$ must be used. Then check the result by computing $AX$.

## Solution

### 1. Determining the Multiplication Side for $A^{-1}$

Given the equation $AX = B$, matrix $A$ is multiplied on the **left** side of the unknown matrix $X$. 

Because matrix multiplication is non-commutative ($AX \neq XA$), we must multiply both sides of the equation by $A^{-1}$ from the **left**:

$$
A^{-1}(AX) = A^{-1}B \implies (A^{-1}A)X = A^{-1}B \implies IX = A^{-1}B \implies X = A^{-1}B
$$

If we had multiplied from the right ($AX A^{-1} = B A^{-1}$), we would obtain $A X A^{-1}$, which does not simplify to $X$. Thus, $A^{-1}$ must be used on the **left**.

### 2. Computing the Inverse Matrix $A^{-1}$

For matrix $A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}$, the determinant is:

$$
\det(A) = (1)(1) - (2)(0) = 1
$$

Using the $2 \times 2$ inverse formula:

$$
A^{-1} = \frac{1}{1} \begin{pmatrix} 1 & -2 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1 & -2 \\ 0 & 1 \end{pmatrix}
$$

### 3. Calculating Matrix $X = A^{-1}B$

Multiplying $A^{-1}$ by $B$ from the left:

$$
X = \begin{pmatrix} 1 & -2 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 3 & 1 \\ 2 & 4 \end{pmatrix}
$$

$$
X = \begin{pmatrix} 1(3) + (-2)(2) & 1(1) + (-2)(4) \\ 0(3) + 1(2) & 0(1) + 1(4) \end{pmatrix}
$$

$$
X = \begin{pmatrix} 3 - 4 & 1 - 8 \\ 0 + 2 & 0 + 4 \end{pmatrix}
$$

$$
X = \begin{pmatrix} -1 & -7 \\ 2 & 4 \end{pmatrix}
$$

### Verification

We check the solution by substituting $X = \begin{pmatrix} -1 & -7 \\ 2 & 4 \end{pmatrix}$ back into $AX$:

$$
AX = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} -1 & -7 \\ 2 & 4 \end{pmatrix}
$$

- **Top-left entry $(1,1)$:** $1(-1) + 2(2) = -1 + 4 = 3$
- **Top-right entry $(1,2)$:** $1(-7) + 2(4) = -7 + 8 = 1$
- **Bottom-left entry $(2,1)$:** $0(-1) + 1(2) = 0 + 2 = 2$
- **Bottom-right entry $(2,2)$:** $0(-7) + 1(4) = 0 + 4 = 4$

Combining the entries gives:

$$
AX = \begin{pmatrix} 3 & 1 \\ 2 & 4 \end{pmatrix} = B
$$

Since $AX = B$, the solution matrix $X = \begin{pmatrix} -1 & -7 \\ 2 & 4 \end{pmatrix}$ is verified to be correct.