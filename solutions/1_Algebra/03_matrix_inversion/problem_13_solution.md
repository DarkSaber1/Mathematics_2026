# Exercise 13 – Inverse of a 3×3 Upper Triangular Matrix

## Problem Statement

Find the inverse of the upper triangular matrix

$$
U=
\begin{pmatrix}
2 & 1 & -1 \\
0 & 3 & 2 \\
0 & 0 & 4
\end{pmatrix}
$$

using Gauss–Jordan elimination. Check your answer by computing $U U^{-1}$.

## Solution

### 1. Step-by-Step Gauss–Jordan Elimination

We form the augmented matrix $[U \mid I_3]$:

$$
[U \mid I_3] = \left(\begin{array}{ccc|ccc} 2 & 1 & -1 & 1 & 0 & 0 \\ 0 & 3 & 2 & 0 & 1 & 0 \\ 0 & 0 & 4 & 0 & 0 & 1 \end{array}\right)
$$

- **Step 1:** Scale row 3 to make its pivot equal to $1$ ($R_3 \leftarrow \frac{1}{4} R_3$):

$$
\left(\begin{array}{ccc|ccc} 2 & 1 & -1 & 1 & 0 & 0 \\ 0 & 3 & 2 & 0 & 1 & 0 \\ 0 & 0 & 1 & 0 & 0 & \frac{1}{4} \end{array}\right)
$$

- **Step 2:** Eliminate the entry in column 3 of row 2 by performing $R_2 \leftarrow R_2 - 2 R_3$:

$$
R_2 \text{ calculation: } (0, 3, 2, 0, 1, 0) - 2\left(0, 0, 1, 0, 0, \frac{1}{4}\right) = \left(0, 3, 0, 0, 1, -\frac{1}{2}\right)
$$

$$
\left(\begin{array}{ccc|ccc} 2 & 1 & -1 & 1 & 0 & 0 \\ 0 & 3 & 0 & 0 & 1 & -\frac{1}{2} \\ 0 & 0 & 1 & 0 & 0 & \frac{1}{4} \end{array}\right)
$$

- **Step 3:** Eliminate the entry in column 3 of row 1 by performing $R_1 \leftarrow R_1 + R_3$:

$$
R_1 \text{ calculation: } (1, 0, 0, 1, 0, 0 \text{ with respect to pivot}) \implies (2, 1, -1, 1, 0, 0) + \left(0, 0, 1, 0, 0, \frac{1}{4}\right) = \left(2, 1, 0, 1, 0, \frac{1}{4}\right)
$$

$$
\left(\begin{array}{ccc|ccc} 2 & 1 & 0 & 1 & 0 & \frac{1}{4} \\ 0 & 3 & 0 & 0 & 1 & -\frac{1}{2} \\ 0 & 0 & 1 & 0 & 0 & \frac{1}{4} \end{array}\right)
$$

- **Step 4:** Scale row 2 to make its pivot equal to $1$ ($R_2 \leftarrow \frac{1}{3} R_2$):

$$
\left(\begin{array}{ccc|ccc} 2 & 1 & 0 & 1 & 0 & \frac{1}{4} \\ 0 & 1 & 0 & 0 & \frac{1}{3} & -\frac{1}{6} \\ 0 & 0 & 1 & 0 & 0 & \frac{1}{4} \end{array}\right)
$$

- **Step 5:** Eliminate the entry in column 2 of row 1 by performing $R_1 \leftarrow R_1 - R_2$:

$$
R_1 \text{ calculation: } \left(2, 1, 0, 1, 0, \frac{1}{4}\right) - \left(0, 1, 0, 0, \frac{1}{3}, -\frac{1}{6}\right) = \left(2, 0, 0, 1, -\frac{1}{3}, \frac{1}{4} + \frac{1}{6}\right) = \left(2, 0, 0, 1, -\frac{1}{3}, \frac{5}{12}\right)
$$

$$
\left(\begin{array}{ccc|ccc} 2 & 0 & 0 & 1 & -\frac{1}{3} & \frac{5}{12} \\ 0 & 1 & 0 & 0 & \frac{1}{3} & -\frac{1}{6} \\ 0 & 0 & 1 & 0 & 0 & \frac{1}{4} \end{array}\right)
$$

- **Step 6:** Scale row 1 by $\frac{1}{2}$ ($R_1 \leftarrow \frac{1}{2} R_1$):

$$
\left(\begin{array}{ccc|ccc} 1 & 0 & 0 & \frac{1}{2} & -\frac{1}{6} & \frac{5}{24} \\ 0 & 1 & 0 & 0 & \frac{1}{3} & -\frac{1}{6} \\ 0 & 0 & 1 & 0 & 0 & \frac{1}{4} \end{array}\right)
$$

Thus, the inverse matrix is:

$$
U^{-1} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{6} & \frac{5}{24} \\ 0 & \frac{1}{3} & -\frac{1}{6} \\ 0 & 0 & \frac{1}{4} \end{pmatrix}
$$

### 2. Verification by Matrix Multiplication

We verify the product $U U^{-1}$:

$$
U U^{-1} = \begin{pmatrix} 2 & 1 & -1 \\ 0 & 3 & 2 \\ 0 & 0 & 4 \end{pmatrix} \begin{pmatrix} \frac{1}{2} & -\frac{1}{6} & \frac{5}{24} \\ 0 & \frac{1}{3} & -\frac{1}{6} \\ 0 & 0 & \frac{1}{4} \end{pmatrix}
$$

- **Row 1 calculations:**
  - $(1,1): 2\left(\frac{1}{2}\right) + 1(0) + (-1)(0) = 1 + 0 + 0 = 1$
  - $(1,2): 2\left(-\frac{1}{6}\right) + 1\left(\frac{1}{3}\right) + (-1)(0) = -\frac{1}{3} + \frac{1}{3} + 0 = 0$
  - $(1,3): 2\left(\frac{5}{24}\right) + 1\left(-\frac{1}{6}\right) + (-1)\left(\frac{1}{4}\right) = \frac{5}{12} - \frac{2}{12} - \frac{3}{12} = 0$

- **Row 2 calculations:**
  - $(2,1): 0\left(\frac{1}{2}\right) + 3(0) + 2(0) = 0$
  - $(2,2): 0\left(-\frac{1}{6}\right) + 3\left(\frac{1}{3}\right) + 2(0) = 0 + 1 + 0 = 1$
  - $(2,3): 0\left(\frac{5}{24}\right) + 3\left(-\frac{1}{6}\right) + 2\left(\frac{1}{4}\right) = 0 - \frac{1}{2} + \frac{1}{2} = 0$

- **Row 3 calculations:**
  - $(3,1): 0\left(\frac{1}{2}\right) + 0(0) + 4(0) = 0$
  - $(3,2): 0\left(-\frac{1}{6}\right) + 0\left(\frac{1}{3}\right) + 4(0) = 0$
  - $(3,3): 0\left(\frac{5}{24}\right) + 0\left(-\frac{1}{6}\right) + 4\left(\frac{1}{4}\right) = 1$

$$
U U^{-1} = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix} = I_3
$$

Since $U U^{-1} = I_3$, the result is verified.