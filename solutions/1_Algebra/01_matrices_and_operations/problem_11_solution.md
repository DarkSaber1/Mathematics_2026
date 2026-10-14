
# Exercise 11 – When Do Matrices Commute?

## Problem Statement

Find the conditions on a, b, c, and d under which AB = BA. Determine the general form of matrix B.

## Solution

Given:

$$
A =
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix}
$$

$$
B =
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
$$

### 1. Calculate AB

$$
AB =
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
$$

$$
AB =
\begin{pmatrix}
a+c & b+d \\
c & d
\end{pmatrix}
$$

### 2. Calculate BA

$$
BA =
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix}
$$

$$
BA =
\begin{pmatrix}
a & a+b \\
c & c+d
\end{pmatrix}
$$

### 3. Find the Conditions

For AB = BA, corresponding entries must be equal.

From the first entry:

$$
a+c=a
$$

$$
c=0
$$

From the second entry:

$$
b+d=a+b
$$

$$
d=a
$$

The remaining entries give the same conditions.

Therefore:

$$
\boxed{c=0,\quad d=a}
$$

### 4. General Form of B

Substituting these conditions:

$$
B =
\begin{pmatrix}
a & b \\
0 & a
\end{pmatrix}
$$

where a and b can be any real numbers.

## Explanation

Two matrices commute when their multiplication order does not affect the result.

To find when AB = BA, we calculate both products and compare their corresponding entries.

The matrices commute only when c = 0 and d = a.

## Verification

Using the general form of B:

$$
AB =
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
a & b \\
0 & a
\end{pmatrix}
$$

$$
AB =
\begin{pmatrix}
a & a+b \\
0 & a
\end{pmatrix}
$$

Now calculate BA:

$$
BA =
\begin{pmatrix}
a & b \\
0 & a
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix}
$$

$$
BA =
\begin{pmatrix}
a & a+b \\
0 & a
\end{pmatrix}
$$

Both results are equal, so the conditions are verified.

## Final Answer

$$
\boxed{c=0,\quad d=a}
$$

The general form of B is:

$$
\boxed{
B =
\begin{pmatrix}
a & b \\
0 & a
\end{pmatrix}
}
$$

where $a,b \in \mathbb{R}$.
