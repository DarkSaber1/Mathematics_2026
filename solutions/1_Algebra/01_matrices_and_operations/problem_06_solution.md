# Exercise 6 – Transpose

## Problem Statement

For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}
$$

compute $A^T$, $B^T$, and $AB$. Then verify in this example that

$$
(AB)^T=B^TA^T.
$$

## Solution

### 1. Calculation of Transposes $A^T$ and $B^T$

The transpose of a matrix is formed by interchanging its rows and columns ($a^T_{ij} = a_{ji}$):

$$
A^T =
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6
\end{pmatrix}
$$

$$
B^T =
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3
\end{pmatrix}
$$

### 2. Calculation of $AB$

Matrix $A$ has size $2 \times 3$ and $B$ has size $3 \times 2$, so the product $AB$ has size $2 \times 2$:

$$
AB =
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3
\end{pmatrix}
=
\begin{pmatrix}
1(1)+2(2)+3(-1) & 1(0)+2(1)+3(3) \\
4(1)+5(2)+6(-1) & 4(0)+5(1)+6(3)
\end{pmatrix}
=
\begin{pmatrix}
2 & 11 \\
8 & 23
\end{pmatrix}
$$

### 3. Verification of $(AB)^T = B^TA^T$

- **Left-hand side $(AB)^T$:**  
  Transposing the resulting product $AB$:

$$
(AB)^T =
\begin{pmatrix}
2 & 11 \\
8 & 23
\end{pmatrix}^T
=
\begin{pmatrix}
2 & 8 \\
11 & 23
\end{pmatrix}
$$

- **Right-hand side $B^TA^T$:**  
  Multiplying $B^T$ (size $2 \times 3$) by $A^T$ (size $3 \times 2$):

$$
B^TA^T =
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3
\end{pmatrix}
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6
\end{pmatrix}
=
\begin{pmatrix}
1(1)+2(2)+(-1)(3) & 1(4)+2(5)+(-1)(6) \\
0(1)+1(2)+3(3) & 0(4)+1(5)+3(6)
\end{pmatrix}
=
\begin{pmatrix}
2 & 8 \\
11 & 23
\end{pmatrix}
$$

### Explanation

Transposing a product reverses the order of the factors, $(AB)^T = B^TA^T$. This reversal occurs because transposing swaps dimensions; multiplying $B^T \cdot A^T$ aligns the inner dimensions correctly ($2 \times 3$ and $3 \times 2$).

### Verification

Comparing both sides:

$$
(AB)^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix} = B^T A^T
$$

Since both expressions evaluate to the exact same matrix, the property $(AB)^T = B^TA^T$ is confirmed.