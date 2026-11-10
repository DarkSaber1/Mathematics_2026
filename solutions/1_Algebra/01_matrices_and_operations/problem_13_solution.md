# Exercise 13 – A Recurrence Written in Matrix Form

## Problem Statement

Let

$$
F=
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}
$$

Compute $F^2$, $F^3$, $F^4$, and $F^5$. Compare the numbers obtained with the sequence

$$
0,1,1,2,3,5,8,\ldots
$$

and describe the relationship you observe. Then compute

$$
F
\begin{pmatrix}
a \\
b \\
\end{pmatrix}
$$

and explain how this multiplication performs one recurrence step: it creates the sum of two consecutive terms and keeps one of them for the next step.

## Solution

### 1. Calculation of Powers $F^2$, $F^3$, $F^4$, and $F^5$

- **Calculation of $F^2$:**

$$
F^2 = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 1(1)+1(1) & 1(1)+1(0) \\ 1(1)+0(1) & 1(1)+0(0) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}
$$

- **Calculation of $F^3$:**

$$
F^3 = F^2 \cdot F = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 2(1)+1(1) & 2(1)+1(0) \\ 1(1)+1(1) & 1(1)+1(0) \end{pmatrix} = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}
$$

- **Calculation of $F^4$:**

$$
F^4 = F^3 \cdot F = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 3(1)+2(1) & 3(1)+2(0) \\ 2(1)+1(1) & 2(1)+1(0) \end{pmatrix} = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix}
$$

- **Calculation of $F^5$:**

$$
F^5 = F^4 \cdot F = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 5(1)+3(1) & 5(1)+3(0) \\ 3(1)+2(1) & 3(1)+2(0) \end{pmatrix} = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}
$$

### 2. Relationship with the Fibonacci Sequence

Let $f_0 = 0, f_1 = 1, f_2 = 1, f_3 = 2, f_4 = 3, f_5 = 5, f_6 = 8, \ldots$ be the Fibonacci sequence defined by $f_{n+1} = f_n + f_{n-1}$.

Comparing the entries of the powers of $F$:
- $F^1 = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} f_2 & f_1 \\ f_1 & f_0 \end{pmatrix}$
- $F^2 = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix} = \begin{pmatrix} f_3 & f_2 \\ f_2 & f_1 \end{pmatrix}$
- $F^3 = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix} = \begin{pmatrix} f_4 & f_3 \\ f_3 & f_2 \end{pmatrix}$
- $F^4 = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix} = \begin{pmatrix} f_5 & f_4 \\ f_4 & f_3 \end{pmatrix}$
- $F^5 = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix} = \begin{pmatrix} f_6 & f_5 \\ f_5 & f_4 \end{pmatrix}$

The general relationship is given by:

$$
F^n = \begin{pmatrix} f_{n+1} & f_n \\ f_n & f_{n-1} \end{pmatrix}
$$

### 3. Matrix Multiplication as a Recurrence Step

Multiplying matrix $F$ by a vector $\begin{pmatrix} a \\ b \end{pmatrix}$:

$$
F \begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} 1(a)+1(b) \\ 1(a)+0(b) \end{pmatrix} = \begin{pmatrix} a+b \\ a \end{pmatrix}
$$

### Explanation

Multiplying a state vector $\begin{pmatrix} a \\ b \end{pmatrix}$ by matrix $F$ executes exactly one step of the Fibonacci recurrence:
1. The top entry becomes $a+b$, calculating the new Fibonacci term by adding two consecutive terms.
2. The bottom entry becomes $a$, shifting the previous top term down to serve as the second term for the subsequent iteration.

### Verification

Let $a = f_4 = 3$ and $b = f_3 = 2$:

$$
F \begin{pmatrix} 3 \\ 2 \end{pmatrix} = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 3 \\ 2 \end{pmatrix} = \begin{pmatrix} 3+2 \\ 3 \end{pmatrix} = \begin{pmatrix} 5 \\ 3 \end{pmatrix} = \begin{pmatrix} f_5 \\ f_4 \end{pmatrix}
$$

The result produces the next pair of consecutive Fibonacci terms $(f_5, f_4) = (5, 3)$, verifying the recurrence behavior.