
# Exercise 13 – A Recurrence Written in Matrix Form

## Problem Statement

Calculate F², F³, F⁴, and F⁵. Compare the results with the Fibonacci sequence and explain how matrix multiplication represents a recurrence step.

## Solution

Given:

$$
F =
\begin{pmatrix}
1 & 1 \\
1 & 0
\end{pmatrix}
$$

### 1. Calculate Matrix Powers

First, calculate F²:

$$
F^2 =
\begin{pmatrix}
1 & 1 \\
1 & 0
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0
\end{pmatrix}
$$

$$
F^2 =
\begin{pmatrix}
2 & 1 \\
1 & 1
\end{pmatrix}
$$

Next, calculate F³:

$$
F^3 =
\begin{pmatrix}
2 & 1 \\
1 & 1
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0
\end{pmatrix}
$$

$$
F^3 =
\begin{pmatrix}
3 & 2 \\
2 & 1
\end{pmatrix}
$$

Now calculate F⁴:

$$
F^4 =
\begin{pmatrix}
3 & 2 \\
2 & 1
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0
\end{pmatrix}
$$

$$
F^4 =
\begin{pmatrix}
5 & 3 \\
3 & 2
\end{pmatrix}
$$

Finally, calculate F⁵:

$$
F^5 =
\begin{pmatrix}
5 & 3 \\
3 & 2
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0
\end{pmatrix}
$$

$$
F^5 =
\begin{pmatrix}
8 & 5 \\
5 & 3
\end{pmatrix}
$$

### 2. Connection to the Fibonacci Sequence

The Fibonacci sequence is:

$$
0,\ 1,\ 1,\ 2,\ 3,\ 5,\ 8,\ldots
$$

Each Fibonacci number is the sum of the two previous numbers.

The powers of F contain consecutive Fibonacci numbers.

The general pattern is:

$$
F^n =
\begin{pmatrix}
f_{n+1} & f_n \\
f_n & f_{n-1}
\end{pmatrix}
$$

where $f_n$ represents the nth Fibonacci number.

### 3. Matrix-Vector Multiplication

Consider the vector:

$$
v =
\begin{pmatrix}
a \\
b
\end{pmatrix}
$$

Multiplying by F:

$$
Fv =
\begin{pmatrix}
1 & 1 \\
1 & 0
\end{pmatrix}
\begin{pmatrix}
a \\
b
\end{pmatrix}
$$

$$
Fv =
\begin{pmatrix}
1(a)+1(b) \\
1(a)+0(b)
\end{pmatrix}
$$

$$
Fv =
\begin{pmatrix}
a+b \\
a
\end{pmatrix}
$$

## Explanation

Matrix F generates Fibonacci numbers through repeated multiplication.

If a and b are two consecutive Fibonacci numbers, multiplying by F produces their sum and keeps a for the next step.

This follows the recurrence relation:

$$
f_{n+1}=f_n+f_{n-1}
$$

## Verification

Using two consecutive Fibonacci numbers:

$$
a=3,\quad b=2
$$

$$
F
\begin{pmatrix}
3 \\
2
\end{pmatrix}
=
\begin{pmatrix}
1 & 1 \\
1 & 0
\end{pmatrix}
\begin{pmatrix}
3 \\
2
\end{pmatrix}
$$

$$
=
\begin{pmatrix}
5 \\
3
\end{pmatrix}
$$

The next Fibonacci number is 5, so the recurrence works correctly.

Also, F⁵ contains the consecutive Fibonacci numbers 8, 5, and 3.

## Final Answer

$$
\boxed{
F^2 =
\begin{pmatrix}
2 & 1 \\
1 & 1
\end{pmatrix}
}
$$

$$
\boxed{
F^3 =
\begin{pmatrix}
3 & 2 \\
2 & 1
\end{pmatrix}
}
$$

$$
\boxed{
F^4 =
\begin{pmatrix}
5 & 3 \\
3 & 2
\end{pmatrix}
}
$$

$$
\boxed{
F^5 =
\begin{pmatrix}
8 & 5 \\
5 & 3
\end{pmatrix}
}
$$

The recurrence step is:

$$
\boxed{
F
\begin{pmatrix}
a \\
b
\end{pmatrix}
=
\begin{pmatrix}
a+b \\
a
\end{pmatrix}
}
$$
