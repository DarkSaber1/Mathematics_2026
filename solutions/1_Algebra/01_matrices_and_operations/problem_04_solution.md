# Exercise 4 – Matrix Multiplication and Noncommutativity

## Problem Statement

For

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

compute $AB$ and $BA$. Is $AB=BA$? Use this example to explain what noncommutativity of matrix multiplication means.

## Solution

### 1. Calculation of $AB$

We compute $AB$ by taking the dot product of rows of $A$ with columns of $B$:

$$
AB =
\begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
3 & 1
\end{pmatrix}
=
\begin{pmatrix}
1(2)+2(3) & 1(0)+2(1) \\
0(2)+1(3) & 0(0)+1(1)
\end{pmatrix}
=
\begin{pmatrix}
8 & 2 \\
3 & 1
\end{pmatrix}
$$

### 2. Calculation of $BA$

We compute $BA$ by taking the dot product of rows of $B$ with columns of $A$:

$$
BA =
\begin{pmatrix}
2 & 0 \\
3 & 1
\end{pmatrix}
\begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix}
=
\begin{pmatrix}
2(1)+0(0) & 2(2)+0(1) \\
3(1)+1(0) & 3(2)+1(1)
\end{pmatrix}
=
\begin{pmatrix}
2 & 4 \\
3 & 7
\end{pmatrix}
$$

### 3. Comparison and Explanation of Noncommutativity

Comparing the entry values of both products:

$$
AB = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix} \neq \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix} = BA
$$

Therefore, $AB \neq BA$. 

In real-number arithmetic, multiplication is commutative ($a \cdot b = b \cdot a$). However, matrix multiplication is **noncommutative** in general; the order in which matrices are multiplied changes which rows are combined with which columns, leading to entirely different results.

### Verification

We verify the entry calculations element-by-element:
- For $AB$:
  - Entry $(1,1): 1 \cdot 2 + 2 \cdot 3 = 8$
  - Entry $(1,2): 1 \cdot 0 + 2 \cdot 1 = 2$
  - Entry $(2,1): 0 \cdot 2 + 1 \cdot 3 = 3$
  - Entry $(2,2): 0 \cdot 0 + 1 \cdot 1 = 1$
- For $BA$:
  - Entry $(1,1): 2 \cdot 1 + 0 \cdot 0 = 2$
  - Entry $(1,2): 2 \cdot 2 + 0 \cdot 1 = 4$
  - Entry $(2,1): 3 \cdot 1 + 1 \cdot 0 = 3$
  - Entry $(2,2): 3 \cdot 2 + 1 \cdot 1 = 7$

Since $8 \neq 2$ and $2 \neq 4$, the inequality $AB \neq BA$ is verified.