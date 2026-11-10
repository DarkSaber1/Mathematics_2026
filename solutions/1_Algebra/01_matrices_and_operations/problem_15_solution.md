# Exercise 15 – Associativity of Multiplication and Different Calculation Paths

## Problem Statement

Given

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\quad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix},\quad C=
\begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix}
$$

Compute $(AB)C$ and $A(BC)$. Compare the results and the number of intermediate operations. Explain what associativity of matrix multiplication means in this example.

## Solution

### 1. Calculation of $(AB)C$ (Path 1)

- **Step 1: Compute $AB$**  
  Matrix $A$ ($2 \times 3$) times matrix $B$ ($3 \times 2$) yields a $2 \times 2$ matrix:

$$
AB = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix} = \begin{pmatrix} 1(1)+2(2)+0(-1) & 1(0)+2(1)+0(3) \\ 0(1)+1(2)+1(-1) & 0(0)+1(1)+1(3) \end{pmatrix} = \begin{pmatrix} 5 & 2 \\ 1 & 4 \end{pmatrix}
$$

- **Step 2: Compute $(AB)C$**  
  Matrix $AB$ ($2 \times 2$) times matrix $C$ ($2 \times 2$) yields a $2 \times 2$ matrix:

$$
(AB)C = \begin{pmatrix} 5 & 2 \\ 1 & 4 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix} = \begin{pmatrix} 5(2)+2(0) & 5(1)+2(-1) \\ 1(2)+4(0) & 1(1)+4(-1) \end{pmatrix} = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}
$$

### 2. Calculation of $A(BC)$ (Path 2)

- **Step 1: Compute $BC$**  
  Matrix $B$ ($3 \times 2$) times matrix $C$ ($2 \times 2$) yields a $3 \times 2$ matrix:

$$
BC = \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix} = \begin{pmatrix} 1(2)+0(0) & 1(1)+0(-1) \\ 2(2)+1(0) & 2(1)+1(-1) \\ -1(2)+3(0) & -1(1)+3(-1) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 4 & 1 \\ -2 & -4 \end{pmatrix}
$$

- **Step 2: Compute $A(BC)$**  
  Matrix $A$ ($2 \times 3$) times matrix $BC$ ($3 \times 2$) yields a $2 \times 2$ matrix:

$$
A(BC) = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 4 & 1 \\ -2 & -4 \end{pmatrix} = \begin{pmatrix} 1(2)+2(4)+0(-2) & 1(1)+2(1)+0(-4) \\ 0(2)+1(4)+1(-2) & 0(1)+1(1)+1(-4) \end{pmatrix} = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}
$$

### 3. Comparison of Results and Operational Complexity

- **Comparison of results:**  
  Both evaluation parenthesizations produce identical matrices:

$$
(AB)C = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix} = A(BC)
$$

- **Comparison of scalar multiplications:**
  - For $M_{m \times n} \cdot N_{n \times p}$, the total number of scalar multiplications required is $m \times n \times p$.
  - **Path 1 $(AB)C$:**  
    Multiplying $A_{2 \times 3} B_{3 \times 2}$ requires $2 \times 3 \times 2 = 12$ scalar multiplications.  
    Multiplying $(AB)_{2 \times 2} C_{2 \times 2}$ requires $2 \times 2 \times 2 = 8$ scalar multiplications.  
    **Total:** $12 + 8 = \mathbf{20\text{ multiplications}}$.
  - **Path 2 $A(BC)$:**  
    Multiplying $B_{3 \times 2} C_{2 \times 2}$ requires $3 \times 2 \times 2 = 12$ scalar multiplications.  
    Multiplying $A_{2 \times 3} (BC)_{3 \times 2}$ requires $2 \times 3 \times 2 = 12$ scalar multiplications.  
    **Total:** $12 + 12 = \mathbf{24\text{ multiplications}}$.

Path $(AB)C$ requires 4 fewer scalar multiplications than $A(BC)$, making it computationally more efficient.

### Explanation of Associativity

Associativity states that when multiplying three or more matrices, the grouping (parenthesization) of factors does not affect the final resulting transformation: $(AB)C = A(BC)$. However, because matrix dimensions determine the total number of scalar calculations, choosing the optimal grouping sequence (known as Matrix Chain Multiplication) significantly impacts computational performance.

### Verification

We confirm that both $(AB)C$ and $A(BC)$ evaluate to $\begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}$ element-by-element:
- Top-left: $10 = 10$
- Top-right: $3 = 3$
- Bottom-left: $2 = 2$
- Bottom-right: $-3 = -3$

The equality verifies associativity and accuracy of intermediate steps.