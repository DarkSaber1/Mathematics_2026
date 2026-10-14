
# Exercise 3 – When Can Matrices Be Multiplied?

## Problem Statement

Determine whether the matrix products AB, BA, BC, CB, AC, CA, AD, and DA are possible. State the dimensions of each valid result.

## Solution

Given matrix dimensions:

- A = 2 x 3
- B = 3 x 4
- C = 4 x 2
- D = 2 x 2

### 1. Checking Matrix Products

| Product | Dimensions | Possible? | Result |
|---------|------------|-----------|--------|
| AB | (2x3)(3x4) | Yes | 2x4 |
| BA | (3x4)(2x3) | No | Undefined |
| BC | (3x4)(4x2) | Yes | 3x2 |
| CB | (4x2)(3x4) | No | Undefined |
| AC | (2x3)(4x2) | No | Undefined |
| CA | (4x2)(2x3) | Yes | 4x3 |
| AD | (2x3)(2x2) | No | Undefined |
| DA | (2x2)(2x3) | Yes | 2x3 |

## Explanation

Matrix multiplication is possible only when the number of columns in the first matrix equals the number of rows in the second matrix.

The resulting matrix has the number of rows of the first matrix and the number of columns of the second matrix.

For example:

$$
(2 \times 3)(3 \times 4) = 2 \times 4
$$

Since the inner dimensions (3 and 3) match, AB is defined.

## Verification

The valid products are:

- AB: 3 = 3
- BC: 4 = 4
- CA: 2 = 2
- DA: 2 = 2

All other products have unequal inner dimensions, so they cannot be multiplied.

## Final Answer

**Defined products:**

- AB = 2 x 4
- BC = 3 x 2
- CA = 4 x 3
- DA = 2 x 3

**Undefined products:**

- BA
- CB
- AC
- AD
