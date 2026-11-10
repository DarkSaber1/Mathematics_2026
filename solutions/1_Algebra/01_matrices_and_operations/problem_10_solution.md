# Exercise 10 – Columns of a Matrix Product

## Problem Statement

Given

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

Denote the columns of $B$ by $b_1,b_2$.

1. Compute $Ab_1$ and $Ab_2$.
2. Compute the matrix $AB$.
3. Compare the results and explain why the columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$.

## Solution

The columns of matrix $B$ are:

$$
b_1 = \begin{pmatrix} 1 \\ -1 \\ 3 \end{pmatrix},\qquad b_2 = \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix}
$$

### 1. Calculation of $Ab_1$ and $Ab_2$

- **Computing $Ab_1$:**

$$
Ab_1 = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ -1 \\ 3 \end{pmatrix} = \begin{pmatrix} 1(1)+2(-1)+0(3) \\ 0(1)+1(-1)+1(3) \end{pmatrix} = \begin{pmatrix} -1 \\ 2 \end{pmatrix}
$$

- **Computing $Ab_2$:**

$$
Ab_2 = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix} = \begin{pmatrix} 1(2)+2(0)+0(1) \\ 0(2)+1(0)+1(1) \end{pmatrix} = \begin{pmatrix} 2 \\ 1 \end{pmatrix}
$$

### 2. Calculation of the Matrix Product $AB$

Multiplying matrix $A$ (size $2 \times 3$) by $B$ (size $3 \times 2$) yields a $2 \times 2$ matrix:

$$
AB = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 2 \\ -1 & 0 \\ 3 & 1 \end{pmatrix} = \begin{pmatrix} 1(1)+2(-1)+0(3) & 1(2)+2(0)+0(1) \\ 0(1)+1(-1)+1(3) & 0(2)+1(0)+1(1) \end{pmatrix} = \begin{pmatrix} -1 & 2 \\ 2 & 1 \end{pmatrix}
$$

### 3. Comparison and Explanation

Comparing the resulting columns:

$$
AB = \begin{pmatrix} -1 & 2 \\ 2 & 1 \end{pmatrix} = \begin{pmatrix} Ab_1 & Ab_2 \end{pmatrix}
$$

- **Column-wise Interpretation of Matrix Multiplication:**  
  By definition of matrix multiplication, the $j$-th column of a product $AB$ is obtained by multiplying the left matrix $A$ by the $j$-th column vector of the right matrix $B$, i.e., $(AB)_{*,j} = A b_j$. Thus, matrix multiplication $AB$ can be viewed as applying the linear transformation $A$ to each column vector of $B$ individually and partitioning the resulting vectors side-by-side.

### Verification

Combining the separately computed vectors $Ab_1$ and $Ab_2$:

$$
\begin{pmatrix} Ab_1 & Ab_2 \end{pmatrix} = \begin{pmatrix} \begin{pmatrix} -1 \\ 2 \end{pmatrix} & \begin{pmatrix} 2 \\ 1 \end{pmatrix} \end{pmatrix} = \begin{pmatrix} -1 & 2 \\ 2 & 1 \end{pmatrix} = AB
$$

The direct matrix product matches the column-by-column construction exactly.