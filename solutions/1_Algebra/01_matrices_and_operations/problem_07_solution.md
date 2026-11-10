# Exercise 7 – Identity Matrix, Zero Matrix, and Powers

## Problem Statement

For

$$
A=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

compute

$$
AI,\qquad IA,\qquad A+0,\qquad A^2,\qquad A^3.
$$

Explain the roles of the matrices $I$ and $0$, and describe the pattern you observe in successive powers of $A$.

## Solution

### 1. Operations with Identity Matrix $I$ and Zero Matrix $0$

Let $I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$ be the $2 \times 2$ identity matrix and $0 = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}$ be the $2 \times 2$ zero matrix.

- **Multiplication by $I$:**

$$
AI = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 2(1)+1(0) & 2(0)+1(1) \\ 0(1)+2(0) & 0(0)+2(1) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}
$$

$$
IA = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 1(2)+0(0) & 1(1)+0(2) \\ 0(2)+1(0) & 0(1)+1(2) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}
$$

- **Addition of $0$:**

$$
A + 0 = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} + \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix} = \begin{pmatrix} 2+0 & 1+0 \\ 0+0 & 2+0 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}
$$

### 2. Calculation of Powers $A^2$ and $A^3$

- **Calculation of $A^2$:**

$$
A^2 = A \cdot A = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 2(2)+1(0) & 2(1)+1(2) \\ 0(2)+2(0) & 0(1)+2(2) \end{pmatrix} = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}
$$

- **Calculation of $A^3$:**

$$
A^3 = A^2 \cdot A = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 4(2)+4(0) & 4(1)+4(2) \\ 0(2)+4(0) & 0(1)+4(2) \end{pmatrix} = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}
$$

### 3. Explanation of Neutral Elements and Observed Pattern

- **Roles of $I$ and $0$:**
  - The identity matrix $I$ serves as the multiplicative neutral element ($AI = IA = A$).
  - The zero matrix $0$ serves as the additive neutral element ($A + 0 = A$).

- **Pattern in Powers $A^n$:**
  Observing the calculated powers:
  - $A^1 = \begin{pmatrix} 2^1 & 1 \cdot 2^0 \\ 0 & 2^1 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$
  - $A^2 = \begin{pmatrix} 2^2 & 2 \cdot 2^1 \\ 0 & 2^2 \end{pmatrix} = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}$
  - $A^3 = \begin{pmatrix} 2^3 & 3 \cdot 2^2 \\ 0 & 2^3 \end{pmatrix} = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}$

  The general pattern for any positive integer $n$ is:

$$
A^n = \begin{pmatrix} 2^n & n \cdot 2^{n-1} \\ 0 & 2^n \end{pmatrix}
$$

### Verification

We test the general formula $A^n = \begin{pmatrix} 2^n & n \cdot 2^{n-1} \\ 0 & 2^n \end{pmatrix}$ against our calculated values:

- For $n = 2$: $\begin{pmatrix} 2^2 & 2 \cdot 2^{2-1} \\ 0 & 2^2 \end{pmatrix} = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix} = A^2$.
- For $n = 3$: $\begin{pmatrix} 2^3 & 3 \cdot 2^{3-1} \\ 0 & 2^3 \end{pmatrix} = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix} = A^3$.

Both match the matrix multiplication results, verifying the pattern.