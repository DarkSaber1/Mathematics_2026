# Exercise 12 – Formula for a Matrix Power

## Problem Statement

Let

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

Compute $A^2$, $A^3$, and $A^4$, and use them to formulate a conjecture for $A^n$. Then do not stop after checking one more case: assume the formula is true for $n$, multiply by $A$, and explain why you obtain exactly the formula for $n+1$.

## Solution

### 1. Calculation of $A^2$, $A^3$, and $A^4$

- **Calculation of $A^2$:**

$$
A^2 = A \cdot A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1(1)+1(0) & 1(1)+1(1) \\ 0(1)+1(0) & 0(1)+1(1) \end{pmatrix} = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}
$$

- **Calculation of $A^3$:**

$$
A^3 = A^2 \cdot A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1(1)+2(0) & 1(1)+2(1) \\ 0(1)+1(0) & 0(1)+1(1) \end{pmatrix} = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}
$$

- **Calculation of $A^4$:**

$$
A^4 = A^3 \cdot A = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1(1)+3(0) & 1(1)+3(1) \\ 0(1)+1(0) & 0(1)+1(1) \end{pmatrix} = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}
$$

### 2. Formulation of Conjecture for $A^n$

Observing the powers of $A$:
- $A^1 = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$
- $A^2 = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}$
- $A^3 = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}$
- $A^4 = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}$

The diagonal entries remain constant as $1$, the lower-left entry remains $0$, while the upper-right entry increases linearly by $1$ with each power $n$. 

Therefore, we conjecture that for any positive integer $n \ge 1$:

$$
A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}
$$

### 3. Proof by Mathematical Induction

We prove the conjecture $P(n): A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}$ for all $n \ge 1$:

- **Base Step ($n = 1$):**  
  For $n = 1$, the formula gives $\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = A^1$, which holds true.

- **Inductive Step:**  
  Assume that the formula holds true for a positive integer $n$ (Inductive Hypothesis):

$$
A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}
$$

  Now, we multiply $A^n$ by $A$ to obtain $A^{n+1}$:

$$
A^{n+1} = A^n \cdot A = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1(1)+n(0) & 1(1)+n(1) \\ 0(1)+1(0) & 0(1)+1(1) \end{pmatrix} = \begin{pmatrix} 1 & n+1 \\ 0 & 1 \end{pmatrix}
$$

  The result is precisely the expression predicted by substituting $(n+1)$ into our general formula.

By the principle of mathematical induction, the formula $A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}$ holds for all integers $n \ge 1$.

### Verification

We test the general formula for $n = 4$:

$$
A^4 = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}
$$

This matches our direct multiplication result $A^4 = A^3 \cdot A = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}$ exactly.