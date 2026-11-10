# Exercise 3 – When Can Matrices Be Multiplied?

## Problem Statement

The matrix sizes are given as:

$$
A_{2\times3},\qquad B_{3\times4},\qquad C_{4\times2},\qquad D_{2\times2}
$$

For the products:

$$
AB,\ BA,\ BC,\ CB,\ AC,\ CA,\ AD,\ DA
$$

determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

## Solution

### 1. Dimension Compatibility Rule

Matrix multiplication $M_{m \times n} \cdot N_{p \times q}$ is defined if and only if the number of columns in the first matrix equals the number of rows in the second matrix ($n = p$). When this condition is met, the resulting matrix has dimensions $m \times q$.

### 2. Evaluation of Matrix Products

| Product | Inner Dimensions Check | Compatibility | Result Size |
| :--- | :--- | :--- | :--- |
| **$AB$** | $A_{2\times 3} \cdot B_{3\times 4} \implies 3 = 3$ | Defined | $2 \times 4$ |
| **$BA$** | $B_{3\times 4} \cdot A_{2\times 3} \implies 4 \neq 2$ | Undefined | — |
| **$BC$** | $B_{3\times 4} \cdot C_{4\times 2} \implies 4 = 4$ | Defined | $3 \times 2$ |
| **$CB$** | $C_{4\times 2} \cdot B_{3\times 4} \implies 2 \neq 3$ | Undefined | — |
| **$AC$** | $A_{2\times 3} \cdot C_{4\times 2} \implies 3 \neq 4$ | Undefined | — |
| **$CA$** | $C_{4\times 2} \cdot A_{2\times 3} \implies 2 = 2$ | Defined | $4 \times 3$ |
| **$AD$** | $A_{2\times 3} \cdot D_{2\times 2} \implies 3 \neq 2$ | Undefined | — |
| **$DA$** | $D_{2\times 2} \cdot A_{2\times 3} \implies 2 = 2$ | Defined | $2 \times 3$ |

### Verification

We verify each case by checking the equality of inner dimensions:

- **$AB$**: Inner dimensions are $3$ and $3$. Since $3 = 3$, $AB$ is valid with size $2 \times 4$.
- **$BA$**: Inner dimensions are $4$ and $2$. Since $4 \neq 2$, $BA$ is invalid.
- **$BC$**: Inner dimensions are $4$ and $4$. Since $4 = 4$, $BC$ is valid with size $3 \times 2$.
- **$CB$**: Inner dimensions are $2$ and $3$. Since $2 \neq 3$, $CB$ is invalid.
- **$AC$**: Inner dimensions are $3$ and $4$. Since $3 \neq 4$, $AC$ is invalid.
- **$CA$**: Inner dimensions are $2$ and $2$. Since $2 = 2$, $CA$ is valid with size $4 \times 3$.
- **$AD$**: Inner dimensions are $3$ and $2$. Since $3 \neq 2$, $AD$ is invalid.
- **$DA$**: Inner dimensions are $2$ and $2$. Since $2 = 2$, $DA$ is valid with size $2 \times 3$.