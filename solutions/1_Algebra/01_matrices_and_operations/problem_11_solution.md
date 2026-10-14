
# Exercise 11 – When Do Matrices Commute?

## Problem Statement

Find the conditions on a, b, c, and d for which AB = BA. Determine the general form of B.

## Solution

Given:

$$
A = \begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix},
\quad
B = \begin{pmatrix}
a & b\\
c & d
\end{pmatrix}
$$

### 1. Calculate AB

$$
AB =
\begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix}
\begin{pmatrix}
a & b\\
c & d
\end{pmatrix}
=
\begin{pmatrix}
a+c & b+d\\
c & d
\end{pmatrix}
$$

### 2. Calculate BA

$$
BA =
\begin{pmatrix}
a & b\\
c & d
\end{pmatrix}
\begin{pmatrix}
1 & 1\\
0 & 1
\end{pmatrix}
=
\begin{pmatrix}
a & a+b\\
c & c+d
\end{pmatrix}
$$

### 3. Find the Conditions

For AB = BA, corresponding entries must be equal.

$$
a+c=a \Rightarrow c=0
$$

$$
b+d=a+b \Rightarrow d=a
$$

The remaining entries give the same conditions.

Therefore:

$$
\boxed{c=0,\quad d=a}
$$

### 4. General Form of B

Substituting the conditions:

$$
\boxed{
B =
\begin{pmatrix}
a & b\\
0 & a
\end{pmatrix}
}
$$

where a and b can be any real numbers.

## Explanation

Two matrices commute when changing their multiplication order does not change the result.

To find when AB = BA, we calculate both products and compare their corresponding entries.

## Verification

Using the general form of B:

$$
AB =
\begin{pmatrix}
a & a+b\\
0 & a
\end{pmatrix}
$$

$$
BA =
\begin{pmatrix}
a & a+b\\
0 & a
\end{pmatrix}
$$

Both products are equal, so the conditions are correct.

## Final Answer

$$
\boxed{c=0,\quad d=a}
$$

$$
\boxed{
B =
\begin{pmatrix}
a & b\\
0 & a
\end{pmatrix},
\quad a,b \in \mathbb{R}
}
$$
