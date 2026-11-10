# Exercise 5 – A 3×3 Matrix

## Problem Statement

Use Gauss–Jordan elimination to find the inverse of

$$
A=
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1
\end{pmatrix}
$$

Check the result by multiplication.

## Solution

### 1. Step-by-Step Gauss–Jordan Elimination

We set up the augmented matrix $[A \mid I]$:

$$
[A \mid I] = \left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 1 & 0 & 1 & 0 & 0 & 1 \end{array}\right)
$$

- **Step 1:** Eliminate the entry below the first pivot in row 3 by performing $R_3 \leftarrow R_3 - R_1$:

$$
R_3 \text{ calculation: } (1, 0, 1, 0, 0, 1) - (1, 1, 0, 1, 0, 0) = (0, -1, 1, -1, 0, 1)
$$

$$
\left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 0 & -1 & 1 & -1 & 0 & 1 \end{array}\right)
$$

- **Step 2:** Eliminate the entry below the second pivot in row 3 by performing $R_3 \leftarrow R_3 + R_2$:

$$
R_3 \text{ calculation: } (0, -1, 1, -1, 0, 1) + (0, 1, 1, 0, 1, 0) = (0, 0, 2, -1, 1, 1)
$$

$$
\left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 0 & 0 & 2 & -1 & 1 & 1 \end{array}\right)
$$

- **Step 3:** Normalize row 3 by multiplying by $\frac{1}{2}$ ($R_3 \leftarrow \frac{1}{2} R_3$):

$$
\left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \end{array}\right)
$$

- **Step 4:** Eliminate the entry above the third pivot in row 2 by performing $R_2 \leftarrow R_2 - R_3$:

$$
R_2 \text{ calculation: } (0, 1, 1, 0, 1, 0) - \left(0, 0, 1, -\frac{1}{2}, \frac{1}{2}, \frac{1}{2}\right) = \left(0, 1, 0, \frac{1}{2}, \frac{1}{2}, -\frac{1}{2}\right)
$$

$$
\left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 0 & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\ 0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \end{array}\right)
$$

- **Step 5:** Eliminate the entry above the second pivot in row 1 by performing $R_1 \leftarrow R_1 - R_2$:

$$
R_1 \text{ calculation: } (1, 1, 0, 1, 0, 0) - \left(0, 1, 0, \frac{1}{2}, \frac{1}{2}, -\frac{1}{2}\right) = \left(1, 0, 0, \frac{1}{2}, -\frac{1}{2}, \frac{1}{2}\right)
$$

$$
\left(\begin{array}{ccc|ccc} 1 & 0 & 0 & \frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\ 0 & 1 & 0 & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\ 0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \end{array}\right)
$$

Since the left submatrix is now $I_3$, the right side is $A^{-1}$:

$$
A^{-1} = \frac{1}{2} \begin{pmatrix} 1 & -1 & 1 \\ 1 & 1 & -1 \\ -1 & 1 & 1 \end{pmatrix}
$$

### 2. Verification by Matrix Multiplication

We test the product $A A^{-1}$:

$$
A A^{-1} = \begin{pmatrix} 1 & 1 & 0 \\ 0 & 1 & 1 \\ 1 & 0 & 1 \end{pmatrix} \left[ \frac{1}{2} \begin{pmatrix} 1 & -1 & 1 \\ 1 & 1 & -1 \\ -1 & 1 & 1 \end{pmatrix} \right]
$$

Factoring out the scalar $\frac{1}{2}$:

$$
A A^{-1} = \frac{1}{2} \begin{pmatrix} 1(1)+1(1)+0(-1) & 1(-1)+1(1)+0(1) & 1(1)+1(-1)+0(1) \\ 0(1)+1(1)+1(-1) & 0(-1)+1(1)+1(1) & 0(1)+1(-1)+1(1) \\ 1(1)+0(1)+1(-1) & 1(-1)+0(1)+1(1) & 1(1)+0(-1)+1(1) \end{pmatrix}
$$

$$
A A^{-1} = \frac{1}{2} \begin{pmatrix} 2 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 2 \end{pmatrix} = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix} = I
$$

Since $A A^{-1} = I$, the result is verified.