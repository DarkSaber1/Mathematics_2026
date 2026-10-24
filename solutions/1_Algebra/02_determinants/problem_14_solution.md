## Exercise 14. A System of Equations and the Determinant

### Problem Definition
Consider the linear system $Ax = b$, where the coefficient matrix $A$ depends on a parameter $k$:[cite: 1]

$$
A = \begin{pmatrix} 1 & 2 \\ k & 4 \end{pmatrix}
$$

1. Determine the values of $k$ for which the system has exactly one solution for every possible right-hand side vector $b$.[cite: 1]
2. For the remaining (exceptional) value of $k$, provide a specific example of a vector $b$ that results in the system having infinitely many solutions.[cite: 1]
3. For the same exceptional value of $k$, provide a specific example of a vector $b$ that results in the system having no solution.[cite: 1]

---

### Detailed Mathematical Solution

#### Step 1: Connecting Determinants to the Number of Solutions

According to the **Invertible Matrix Theorem**, a square linear system $Ax = b$ has a unique (exactly one) solution for every vector $b$ if and only if the coefficient matrix $A$ is invertible.[cite: 1] 

Matrix $A$ is invertible if and only if its determinant is non-zero ($\det A \neq 0$).[cite: 1]

Let us compute $\det A$:

$$
\det A = \det \begin{pmatrix} 1 & 2 \\ k & 4 \end{pmatrix} = (1 \cdot 4) - (2 \cdot k) = 4 - 2k
$$

To find when the system has a unique solution, we set the determinant to be non-zero:

$$
4 - 2k \neq 0 \implies 2k \neq 4 \implies k \neq 2
$$

**Conclusion for Part 1:** The system has exactly one solution for every $b$ for all real numbers $k$ such that **$k \neq 2$**.[cite: 1]

---

#### Step 2: Analyzing the Exceptional Case ($k = 2$)

The "remaining value" of the parameter is $k = 2$.[cite: 1] 

Let us substitute $k = 2$ back into matrix $A$:

$$
A = \begin{pmatrix} 1 & 2 \\ 2 & 4 \end{pmatrix}
$$

The system of equations $Ax = b$ (where $x = \begin{pmatrix} x_1 \\ x_2 \end{pmatrix}$ and $b = \begin{pmatrix} b_1 \\ b_2 \end{pmatrix}$) becomes:

$$
\begin{cases}
1x_1 + 2x_2 = b_1 \\
2x_1 + 4x_2 = b_2
\end{cases}
$$

Notice that the left-hand side of the second equation is exactly twice the left-hand side of the first equation ($2x_1 + 4x_2 = 2(x_1 + 2x_2)$). 

Because the determinant is zero ($\det A = 4 - 2(2) = 0$), the system is singular and will either have **infinitely many solutions** (if the equations are consistent) or **no solution** (if the equations contradict each other).

---

#### Step 3: Finding a Vector $b$ for Infinitely Many Solutions

To have infinitely many solutions, the two equations must describe the exact same line. This means the right-hand sides must share the same proportionality as the left-hand sides.

Since the left side of Equation 2 is twice Equation 1, we must require:

$$
b_2 = 2 \cdot b_1
$$

Let us choose a simple value for $b_1$, for example, $b_1 = 1$. Then $b_2 = 2(1) = 2$.

$$
b = \begin{pmatrix} 1 \\ 2 \end{pmatrix}
$$

**Verification:**
The system becomes:
$$
\begin{cases}
x_1 + 2x_2 = 1 \\
2x_1 + 4x_2 = 2 \implies x_1 + 2x_2 = 1
\end{cases}
$$
Both equations are identical. Any point on the line $x_1 + 2x_2 = 1$ (such as $(1, 0)$ or $(-1, 1)$) is a valid solution, meaning there are infinitely many solutions.[cite: 1]

---

#### Step 4: Finding a Vector $b$ for No Solution

To have no solution, the two equations must describe parallel, non-intersecting lines. This happens when the left-hand sides are proportional, but the right-hand sides break that proportionality (creating a logical contradiction).

We need:

$$
b_2 \neq 2 \cdot b_1
$$

Let us choose $b_1 = 1$. Instead of $2$, let us choose $b_2 = 5$.

$$
b = \begin{pmatrix} 1 \\ 5 \end{pmatrix}
$$

**Verification:**
The system becomes:
$$
\begin{cases}
x_1 + 2x_2 = 1 \\
2x_1 + 4x_2 = 5
\end{cases}
$$
If we multiply the first equation by 2, we get $2x_1 + 4x_2 = 2$. But the second equation states $2x_1 + 4x_2 = 5$. 
Since $2 \neq 5$, this is a mathematical impossibility. The system is inconsistent and has no solution.[cite: 1]

---

### Conclusion and Key Takeaways

1. **Unique Solution Condition:**
   The system has exactly one solution for all $b$ when **$k \neq 2$** (because $\det A \neq 0$).[cite: 1]

2. **Infinitely Many Solutions Example:**
   For $k = 2$, choosing **$b = \begin{pmatrix} 1 \\ 2 \end{pmatrix}$** makes the equations consistent and redundant.[cite: 1]

3. **No Solution Example:**
   For $k = 2$, choosing **$b = \begin{pmatrix} 1 \\ 5 \end{pmatrix}$** creates parallel lines and a mathematical contradiction, resulting in no solution.[cite: 1]