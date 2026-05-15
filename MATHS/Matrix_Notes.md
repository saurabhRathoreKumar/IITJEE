# IIT JEE Advanced & Mains: Comprehensive Matrix Notes

## Table of Contents
1. [Basic Concepts](#basic-concepts)
2. [Types of Matrices](#types-of-matrices)
3. [Matrix Operations](#matrix-operations)
4. [Determinants](#determinants)
5. [Matrix Inverse](#matrix-inverse)
6. [Rank of a Matrix](#rank-of-a-matrix)
7. [System of Linear Equations](#system-of-linear-equations)
8. [Eigenvalues & Eigenvectors](#eigenvalues--eigenvectors)
9. [IIT JEE Problems with Solutions](#iit-jee-problems-with-solutions)
10. [Important Theorems](#important-theorems)

---

## Basic Concepts

### What is a Matrix?

A matrix is a rectangular arrangement of numbers (real or complex) in rows and columns, enclosed in brackets.

**General Notation:**
```
      [a₁₁  a₁₂  a₁₃  ...  a₁ₙ]
      [a₂₁  a₂₂  a₂₃  ...  a₂ₙ]
A =   [a₃₁  a₃₂  a₃₃  ...  a₃ₙ]
      [  ⋮    ⋮    ⋮   ⋱    ⋮  ]
      [aₘ₁  aₘ₂  aₘ₃  ...  aₘₙ]
```

**Order of Matrix:** An m×n matrix has `m` rows and `n` columns.
- Example: A 2×3 matrix has 2 rows and 3 columns
- Total elements = m × n

### Visual Representation:

```
        Column 1   Column 2   Column 3
Row 1   [   5      -3         2     ]
Row 2   [   1       4        -1     ]
        Order: 2×3
```

### Example: 2×3 Matrix
$$A = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}$$

This is a 2×3 matrix (2 rows, 3 columns) with 6 total elements.

---

## Types of Matrices

### 1. **Row Matrix**
A matrix with only one row (1×n matrix).

**Row Matrix A (1×4):**
$$A = \begin{bmatrix} 2 & 5 & -3 & 7 \end{bmatrix}$$

### 2. **Column Matrix**
A matrix with only one column (m×1 matrix).

**Column Matrix B (3×1):**
$$B = \begin{bmatrix} 3 \\ 7 \\ -2 \end{bmatrix}$$

### 3. **Square Matrix**
Number of rows = Number of columns (n×n matrix).

**Square Matrix C (2×2):**
$$C = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}$$

### 4. **Diagonal Matrix**
A square matrix where all non-diagonal elements are zero.

**Diagonal Matrix D (3×3):**
$$D = \begin{bmatrix} 5 & 0 & 0 \\ 0 & 3 & 0 \\ 0 & 0 & 2 \end{bmatrix}$$

### 5. **Identity Matrix (I)**
A diagonal matrix where all diagonal elements are 1.

**Identity Matrix (3×3):**
$$I_3 = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$$

**Property:** A·I = A for any matrix A

### 6. **Null/Zero Matrix**
All elements are zero.

**Null Matrix O (2×2):**
$$O = \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix}$$

### 7. **Triangular Matrices**

**Upper Triangular U (3×3):**
- All elements below the diagonal are zero
$$U = \begin{bmatrix} 2 & 3 & 5 \\ 0 & 1 & 4 \\ 0 & 0 & 6 \end{bmatrix}$$

**Lower Triangular L (3×3):**
- All elements above the diagonal are zero
$$L = \begin{bmatrix} 3 & 0 & 0 \\ 2 & 5 & 0 \\ 1 & 4 & 7 \end{bmatrix}$$

### 8. **Symmetric Matrix**
Where $A^T = A$ (Transpose equals the original matrix)

**Symmetric Matrix S (3×3):**
$$S = \begin{bmatrix} 1 & 2 & 3 \\ 2 & 5 & 4 \\ 3 & 4 & 7 \end{bmatrix}$$

**Property:** Notice that $a_{ij} = a_{ji}$ (elements are symmetric about diagonal)

### 9. **Skew-Symmetric Matrix**
Where $A^T = -A$ (Transpose equals negative of original)

**Skew-Symmetric Matrix K (3×3):**
$$K = \begin{bmatrix} 0 & 2 & -3 \\ -2 & 0 & 4 \\ 3 & -4 & 0 \end{bmatrix}$$

**Properties:** 
- All diagonal elements are 0
- Elements satisfy $a_{ij} = -a_{ji}$

### 10. **Orthogonal Matrix**
$$A^T·A = I$$

**Property:** $A^{-1} = A^T$

### 11. **Idempotent Matrix**
$$A^2 = A$$

### 12. **Involutory Matrix**
$$A^2 = I$$

---

## Matrix Operations

### 1. **Equality of Matrices**
Two matrices are equal if:
- They have the same order
- Corresponding elements are equal

$$A = B \Rightarrow a_{ij} = b_{ij} \text{ for all } i, j$$

### 2. **Addition and Subtraction**
Matrices can be added/subtracted if they have the same order.

**Rule:** Add/subtract corresponding elements

$$A + B = \begin{bmatrix} a_{11}+b_{11} & a_{12}+b_{12} \\ a_{21}+b_{21} & a_{22}+b_{22} \end{bmatrix}$$

**Example:**
$$\begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} + \begin{bmatrix} 5 & 6 \\ 7 & 8 \end{bmatrix} = \begin{bmatrix} 6 & 8 \\ 10 & 12 \end{bmatrix}$$

**Properties:**
- A + B = B + A (Commutative)
- (A + B) + C = A + (B + C) (Associative)
- A + O = A (Identity)

### 3. **Scalar Multiplication**
Each element is multiplied by the scalar.

$$kA = \begin{bmatrix} ka_{11} & ka_{12} \\ ka_{21} & ka_{22} \end{bmatrix}$$

**Example:**
$$3\begin{bmatrix} 2 & -1 \\ 4 & 3 \end{bmatrix} = \begin{bmatrix} 6 & -3 \\ 12 & 9 \end{bmatrix}$$

### 4. **Matrix Multiplication**

For multiplication A(m×n) × B(n×p), result is C(m×p).

**Condition:** Number of columns in first = Number of rows in second

**Rule:** Each element $c_{ij}$ is the dot product of row i of A and column j of B.

$$c_{ij} = \sum_{k=1}^{n} a_{ik} \cdot b_{kj}$$

**Example: Multiply Two 2×2 Matrices**

**Step 1: Setup the multiplication**
$$\begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} \times \begin{bmatrix} 5 & 6 \\ 7 & 8 \end{bmatrix}$$

**Step 2: Calculate each element**
$$= \begin{bmatrix} 1(5)+2(7) & 1(6)+2(8) \\ 3(5)+4(7) & 3(6)+4(8) \end{bmatrix}$$

**Step 3: Final Result**
$$= \begin{bmatrix} 19 & 22 \\ 43 & 50 \end{bmatrix}$$

**Properties:**
- (AB)C = A(BC) (Associative)
- A(B+C) = AB + AC (Distributive)
- AB ≠ BA in general (NOT Commutative)
- AI = A and IA = A

### 5. **Transpose of a Matrix**

Interchanging rows and columns.

**Original Matrix A (2×3):**
$$A = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}$$

**Transposed Matrix A^T (3×2):**
$$A^T = \begin{bmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{bmatrix}$$

*Note: Rows become columns and columns become rows*

**Properties:**
- $(A^T)^T = A$
- $(A + B)^T = A^T + B^T$
- $(AB)^T = B^T A^T$ (Order reverses!)
- $(kA)^T = kA^T$

---

## Determinants

### Definition
A determinant is a scalar value associated with a square matrix.

**Notation:** det(A) or |A|

### For 2×2 Matrix:

$$\begin{vmatrix} a & b \\ c & d \end{vmatrix} = ad - bc$$

**Example:**
$$\begin{vmatrix} 3 & 5 \\ 2 & 4 \end{vmatrix} = 3(4) - 5(2) = 12 - 10 = 2$$

### For 3×3 Matrix (Expansion by First Row):

$$\begin{vmatrix} a & b & c \\ d & e & f \\ g & h & i \end{vmatrix} = a\begin{vmatrix} e & f \\ h & i \end{vmatrix} - b\begin{vmatrix} d & f \\ g & i \end{vmatrix} + c\begin{vmatrix} d & e \\ g & h \end{vmatrix}$$

$$= a(ei - fh) - b(di - fg) + c(dh - eg)$$

**Example:**
$$\begin{vmatrix} 1 & 2 & 3 \\ 0 & 4 & 5 \\ 1 & 0 & 6 \end{vmatrix}$$

$$= 1\begin{vmatrix} 4 & 5 \\ 0 & 6 \end{vmatrix} - 2\begin{vmatrix} 0 & 5 \\ 1 & 6 \end{vmatrix} + 3\begin{vmatrix} 0 & 4 \\ 1 & 0 \end{vmatrix}$$

$$= 1(24-0) - 2(0-5) + 3(0-4) = 24 + 10 - 12 = 22$$

### Properties of Determinants:

1. **det(A) = det(A^T)**
   - Determinant of transpose equals original determinant

2. **If two rows (or columns) are identical, det(A) = 0**

3. **If a row (or column) is all zeros, det(A) = 0**

4. **Swapping two rows changes sign of determinant**
   - det after swap = -det(original)

5. **Multiplying a row by scalar k multiplies determinant by k**
   - det(kA) = k^n · det(A) where A is n×n

6. **det(AB) = det(A) · det(B)**
   - Determinant of product = Product of determinants

7. **If det(A) ≠ 0, matrix is invertible (non-singular)**

8. **Adding multiple of one row to another row doesn't change determinant**

### Visualization: 3×3 Determinant Expansion

```
        | a  b  c |
        | d  e  f |  = a·(ei-fh) - b·(di-fg) + c·(dh-eg)
        | g  h  i |

Step 1: Pick row (usually first row: a, b, c)
Step 2: For each element, find minor (2×2 determinant)
Step 3: Apply (+,-,+,-...) pattern of signs (Checkerboard)
```

---

## Matrix Inverse

### Definition
If A·B = B·A = I, then B is the inverse of A, denoted as A⁻¹.

**Condition:** Matrix must be square and det(A) ≠ 0 (non-singular)

### For 2×2 Matrix:

$$A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}, \quad A^{-1} = \frac{1}{ad-bc}\begin{bmatrix} d & -b \\ -c & a \end{bmatrix}$$

**Example:**
$$A = \begin{bmatrix} 4 & 7 \\ 2 & 6 \end{bmatrix}$$

$$\text{det}(A) = 4(6) - 7(2) = 24 - 14 = 10$$

$$A^{-1} = \frac{1}{10}\begin{bmatrix} 6 & -7 \\ -2 & 4 \end{bmatrix} = \begin{bmatrix} 0.6 & -0.7 \\ -0.2 & 0.4 \end{bmatrix}$$

### For General n×n Matrix:

$$A^{-1} = \frac{1}{\text{det}(A)} \cdot \text{adj}(A)$$

Where **adj(A)** (adjugate matrix) = Transpose of cofactor matrix

**Steps to find:**
1. Find cofactor matrix (with alternating signs)
2. Transpose it to get adjugate
3. Divide by determinant

### Properties:
- $(A^{-1})^{-1} = A$
- $(AB)^{-1} = B^{-1}A^{-1}$ (Order reverses!)
- $(A^{-1})^T = (A^T)^{-1}$
- det(A^{-1}) = 1/det(A)

### Verification:
Always verify: A·A^{-1} = I

---

## Rank of a Matrix

### Definition
The rank of a matrix is the maximum number of linearly independent rows (or columns).

**Notation:** rank(A) or ρ(A)

### Properties:
1. **For m×n matrix:** rank(A) ≤ min(m, n)
2. **For square n×n matrix:** 
   - rank(A) = n ⟺ det(A) ≠ 0 (Full rank)
   - rank(A) < n ⟺ det(A) = 0 (Singular)
3. **rank(A^T) = rank(A)**
4. **rank(AB) ≤ min(rank(A), rank(B))**

### How to Find Rank:
Use **Row Echelon Form (REF)** - reduce to triangular form using row operations.

**Example:**
$$A = \begin{bmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 1 & 2 & 3 \end{bmatrix}$$

Row₂ - 2·Row₁: $\begin{bmatrix} 1 & 2 & 3 \\ 0 & 0 & 0 \\ 1 & 2 & 3 \end{bmatrix}$

Row₃ - Row₁: $\begin{bmatrix} 1 & 2 & 3 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix}$

**Number of non-zero rows = 1**, so **rank(A) = 1**

---

## System of Linear Equations

### General Form:
$$\begin{cases}
a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n = b_1 \\
a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n = b_2 \\
\vdots \\
a_{m1}x_1 + a_{m2}x_2 + \cdots + a_{mn}x_n = b_m
\end{cases}$$

### Matrix Form:
$$AX = B$$

Where:
- **A** = Coefficient matrix (m×n)
- **X** = Variable matrix (n×1)
- **B** = Constant matrix (m×1)

### Solving Using Matrix Inverse:

If det(A) ≠ 0:
$$X = A^{-1}B$$

### Consistency of System:

1. **Consistent and Unique Solution:**
   - rank(A) = rank([A|B]) = n

2. **Consistent and Infinite Solutions:**
   - rank(A) = rank([A|B]) < n

3. **Inconsistent (No Solution):**
   - rank(A) ≠ rank([A|B])

### Example:
$$\begin{cases}
2x + 3y = 8 \\
x - y = 1
\end{cases}$$

Matrix form: $\begin{bmatrix} 2 & 3 \\ 1 & -1 \end{bmatrix}\begin{bmatrix} x \\ y \end{bmatrix} = \begin{bmatrix} 8 \\ 1 \end{bmatrix}$

$$\text{det}(A) = 2(-1) - 3(1) = -5 \neq 0$$

Solution exists and is unique:
$$\begin{bmatrix} x \\ y \end{bmatrix} = \frac{1}{-5}\begin{bmatrix} -1 & -3 \\ -1 & 2 \end{bmatrix}\begin{bmatrix} 8 \\ 1 \end{bmatrix} = \begin{bmatrix} 2 \\ 1 \end{bmatrix}$$

---

## Eigenvalues & Eigenvectors

### Definition

For a square matrix A, if there exist scalar λ and non-zero vector v such that:
$$Av = λv$$

Then:
- **λ** is called an **eigenvalue**
- **v** is called an **eigenvector** corresponding to λ

### Finding Eigenvalues:

**Characteristic Equation:**
$$\text{det}(A - λI) = 0$$

**Example:**
$$A = \begin{bmatrix} 4 & 1 \\ 2 & 3 \end{bmatrix}$$

$$\text{det}\begin{bmatrix} 4-λ & 1 \\ 2 & 3-λ \end{bmatrix} = 0$$

$$(4-λ)(3-λ) - 2 = 0$$

$$12 - 4λ - 3λ + λ^2 - 2 = 0$$

$$λ^2 - 7λ + 10 = 0$$

$$(λ - 5)(λ - 2) = 0$$

**Eigenvalues:** λ₁ = 5, λ₂ = 2

### Finding Eigenvectors:

For each eigenvalue λ, solve $(A - λI)v = 0$

**For λ₁ = 5:**
$$\begin{bmatrix} -1 & 1 \\ 2 & -2 \end{bmatrix}\begin{bmatrix} v_1 \\ v_2 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \end{bmatrix}$$

$$-v_1 + v_2 = 0 \Rightarrow v_1 = v_2$$

**Eigenvector:** $v = \begin{bmatrix} 1 \\ 1 \end{bmatrix}$

**For λ₂ = 2:**
$$\begin{bmatrix} 2 & 1 \\ 2 & 1 \end{bmatrix}\begin{bmatrix} v_1 \\ v_2 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \end{bmatrix}$$

$$2v_1 + v_2 = 0 \Rightarrow v_2 = -2v_1$$

**Eigenvector:** $v = \begin{bmatrix} 1 \\ -2 \end{bmatrix}$

### Properties:
1. **Sum of eigenvalues = Trace(A)** = sum of diagonal elements
2. **Product of eigenvalues = det(A)**
3. **Number of eigenvalues = order of matrix**
4. If A is symmetric, all eigenvalues are real
5. Eigenvectors corresponding to different eigenvalues are linearly independent

---

## IIT JEE Problems with Solutions

### **Problem 1 (Matrix Multiplication & Determinant)**

**Question:** If $A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}$ and $B = \begin{bmatrix} 5 & 6 \\ 7 & 8 \end{bmatrix}$, find det(AB).

**Solution:**

**Method 1: Using Property det(AB) = det(A)·det(B)**

$$\text{det}(A) = 1(4) - 2(3) = 4 - 6 = -2$$

$$\text{det}(B) = 5(8) - 6(7) = 40 - 42 = -2$$

$$\text{det}(AB) = \text{det}(A) \times \text{det}(B) = (-2) \times (-2) = 4$$

**Method 2: Direct Calculation**

**Step 1: Calculate AB**
$$AB = \begin{bmatrix} 1(5)+2(7) & 1(6)+2(8) \\ 3(5)+4(7) & 3(6)+4(8) \end{bmatrix}$$

**Step 2: Simplify**
$$AB = \begin{bmatrix} 19 & 22 \\ 43 & 50 \end{bmatrix}$$

**Step 3: Calculate determinant**
$$\text{det}(AB) = 19(50) - 22(43) = 950 - 946 = 4$$ ✓

---

### **Problem 2 (Matrix Inverse & System of Equations)**

**Question:** Solve the system using matrix method:
$$\begin{cases}
2x + y = 5 \\
x + 3y = 5
\end{cases}$$

**Solution:**

Matrix form: $\begin{bmatrix} 2 & 1 \\ 1 & 3 \end{bmatrix}\begin{bmatrix} x \\ y \end{bmatrix} = \begin{bmatrix} 5 \\ 5 \end{bmatrix}$

Let $A = \begin{bmatrix} 2 & 1 \\ 1 & 3 \end{bmatrix}$

$$\text{det}(A) = 2(3) - 1(1) = 6 - 1 = 5 \neq 0$$

$$A^{-1} = \frac{1}{5}\begin{bmatrix} 3 & -1 \\ -1 & 2 \end{bmatrix}$$

**Step 1: Multiply A⁻¹ by B**
$$\begin{bmatrix} x \\ y \end{bmatrix} = \frac{1}{5}\begin{bmatrix} 3 & -1 \\ -1 & 2 \end{bmatrix}\begin{bmatrix} 5 \\ 5 \end{bmatrix}$$

**Step 2: Simplify**
$$= \frac{1}{5}\begin{bmatrix} 15-5 \\ -5+10 \end{bmatrix}$$

**Step 3: Final result**
$$= \frac{1}{5}\begin{bmatrix} 10 \\ 5 \end{bmatrix} = \begin{bmatrix} 2 \\ 1 \end{bmatrix}$$

**Answer:** x = 2, y = 1

**Verification:**
- 2(2) + 1 = 5 ✓
- 2 + 3(1) = 5 ✓

---

### **Problem 3 (Symmetric & Skew-Symmetric Decomposition)**

**Question:** Express $A = \begin{bmatrix} 2 & 3 & 1 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{bmatrix}$ as sum of symmetric and skew-symmetric matrices.

**Solution:**

Any matrix can be written as: $A = \frac{A+A^T}{2} + \frac{A-A^T}{2}$

Where the first part is symmetric and second is skew-symmetric.

$$A^T = \begin{bmatrix} 2 & 4 & 7 \\ 3 & 5 & 8 \\ 1 & 6 & 9 \end{bmatrix}$$

$$A + A^T = \begin{bmatrix} 4 & 7 & 8 \\ 7 & 10 & 14 \\ 8 & 14 & 18 \end{bmatrix}$$

**Symmetric part:**
$$P = \frac{A+A^T}{2} = \begin{bmatrix} 2 & 3.5 & 4 \\ 3.5 & 5 & 7 \\ 4 & 7 & 9 \end{bmatrix}$$

$$A - A^T = \begin{bmatrix} 0 & -1 & -6 \\ 1 & 0 & -2 \\ 6 & 2 & 0 \end{bmatrix}$$

**Skew-Symmetric part:**
$$Q = \frac{A-A^T}{2} = \begin{bmatrix} 0 & -0.5 & -3 \\ 0.5 & 0 & -1 \\ 3 & 1 & 0 \end{bmatrix}$$

**Verification:** P + Q = A ✓

---

### **Problem 4 (Eigenvalues & Trace)**

**Question:** If A is a 2×2 matrix with eigenvalues 3 and 5, and a₁₁ = 2, find a₂₂.

**Solution:**

From the property: **Sum of eigenvalues = Trace(A)**

$$3 + 5 = a_{11} + a_{22}$$

$$8 = 2 + a_{22}$$

$$a_{22} = 6$$

---

### **Problem 5 (Rank of Matrix)**

**Question:** Find the rank of:
$$A = \begin{bmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 3 & 6 & 9 \end{bmatrix}$$

**Solution:**

Apply row operations:

$$\begin{bmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 3 & 6 & 9 \end{bmatrix}$$

R₂ → R₂ - 2R₁:
$$\begin{bmatrix} 1 & 2 & 3 \\ 0 & 0 & 0 \\ 3 & 6 & 9 \end{bmatrix}$$

R₃ → R₃ - 3R₁:
$$\begin{bmatrix} 1 & 2 & 3 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix}$$

**Number of non-zero rows = 1**

**Rank(A) = 1**

Notice: Column 2 = 2·Column 1, Column 3 = 3·Column 1 (Linear dependence)

---

### **Problem 6 (Matrix Equation)**

**Question:** If $A = \begin{bmatrix} 1 & 2 \\ 0 & 3 \end{bmatrix}$ and $AX = \begin{bmatrix} 5 \\ 6 \end{bmatrix}$, find X.

**Solution:**

$$X = A^{-1}\begin{bmatrix} 5 \\ 6 \end{bmatrix}$$

$$\text{det}(A) = 1(3) - 2(0) = 3$$

$$A^{-1} = \frac{1}{3}\begin{bmatrix} 3 & -2 \\ 0 & 1 \end{bmatrix} = \begin{bmatrix} 1 & -2/3 \\ 0 & 1/3 \end{bmatrix}$$

$$X = \begin{bmatrix} 1 & -2/3 \\ 0 & 1/3 \end{bmatrix}\begin{bmatrix} 5 \\ 6 \end{bmatrix} = \begin{bmatrix} 5-4 \\ 0+2 \end{bmatrix} = \begin{bmatrix} 1 \\ 2 \end{bmatrix}$$

**Answer:** $X = \begin{bmatrix} 1 \\ 2 \end{bmatrix}$

---

### **Problem 7 (Determinant Properties - IIT Advanced)**

**Question:** If $A = \begin{bmatrix} 0 & a & b \\ -a & 0 & c \\ -b & -c & 0 \end{bmatrix}$, show that det(A) = 0.

**Solution:**

This is a skew-symmetric matrix (A^T = -A).

For any skew-symmetric matrix of odd order (3×3), the determinant is always 0.

**Proof using determinant properties:**

$$\text{det}(A^T) = \text{det}(-A) = (-1)^3 \text{det}(A) = -\text{det}(A)$$

But also: $\text{det}(A^T) = \text{det}(A)$ (transpose property)

Therefore: $\text{det}(A) = -\text{det}(A)$

$$2·\text{det}(A) = 0$$

$$\text{det}(A) = 0$$ ✓

---

### **Problem 8 (Consistency of System - IIT Mains)**

**Question:** For what values of λ and μ does the system have:
- Unique solution?
- No solution?
- Infinite solutions?

$$\begin{cases}
x + y + z = 6 \\
x + 2y + 3z = 10 \\
x + 2y + λz = μ
\end{cases}$$

**Solution:**

Coefficient matrix:
$$A = \begin{bmatrix} 1 & 1 & 1 \\ 1 & 2 & 3 \\ 1 & 2 & λ \end{bmatrix}$$

$$\text{det}(A) = 1(2λ-6) - 1(λ-3) + 1(2-2)$$
$$= 2λ - 6 - λ + 3 = λ - 3$$

**Case 1: Unique Solution**
- det(A) ≠ 0, i.e., **λ ≠ 3**
- μ can be any value

**Case 2: No Solution**
- λ = 3 and rank(A) ≠ rank([A|B])
- When λ = 3, the third equation becomes: x + 2y + 3z = μ
- This contradicts the second equation unless μ = 10
- **λ = 3 and μ ≠ 10**

**Case 3: Infinite Solutions**
- λ = 3 and rank(A) = rank([A|B])
- **λ = 3 and μ = 10**

---

### **Problem 9 (Idempotent Matrix)**

**Question:** If A is an idempotent matrix (A² = A), prove that (I - A)² = I - A.

**Solution:**

$$(I - A)^2 = I^2 - IA - AI + A^2$$

$$= I - A - A + A^2$$

Since A² = A (given):
$$= I - 2A + A$$

$$= I - A$$ ✓

This proves (I - A) is also idempotent.

---

### **Problem 10 (Trace and Determinant - Advanced)**

**Question:** If A is a 3×3 matrix with eigenvalues 2, -1, and 3, find:
- Trace(A)
- det(A)
- A is singular or non-singular?

**Solution:**

**Trace(A) = Sum of eigenvalues**
$$\text{Trace}(A) = 2 + (-1) + 3 = 4$$

**det(A) = Product of eigenvalues**
$$\text{det}(A) = 2 × (-1) × 3 = -6$$

**det(A) ≠ 0, so A is non-singular**

---

## Important Theorems

### 1. **Cayley-Hamilton Theorem**
Every square matrix satisfies its own characteristic equation.

If characteristic equation is: $λ^2 - 5λ + 6 = 0$

Then: $A^2 - 5A + 6I = 0$

### 2. **Rank-Nullity Theorem**
For m×n matrix A:
$$\text{rank}(A) + \text{nullity}(A) = n$$

where nullity(A) = dimension of null space

### 3. **Properties of Orthogonal Matrices**
- A^T·A = I
- det(A) = ±1
- A^{-1} = A^T
- Preserve lengths and angles

### 4. **Spectral Theorem**
For symmetric matrix A with orthonormal eigenvectors:
$$A = PDP^T$$

where P = matrix of eigenvectors, D = diagonal matrix of eigenvalues

### 5. **Matrix Similarity**
If B = P^{-1}AP, then A and B are similar and have:
- Same eigenvalues
- Same trace
- Same determinant
- Same rank

### 6. **Diagonalization Condition**
An n×n matrix A is diagonalizable if and only if it has n linearly independent eigenvectors.

---

## Quick Reference: Matrix Formulas

| Concept | Formula |
|---------|---------|
| Matrix Multiplication | $c_{ij} = \sum_{k} a_{ik}b_{kj}$ |
| 2×2 Determinant | $ad - bc$ |
| 2×2 Inverse | $\frac{1}{ad-bc}\begin{bmatrix} d & -b \\ -c & a \end{bmatrix}$ |
| General Inverse | $A^{-1} = \frac{\text{adj}(A)}{\text{det}(A)}$ |
| Transpose | Swap rows and columns |
| Trace | Sum of diagonal elements |
| Eigenvalue Equation | det(A - λI) = 0 |
| Characteristic Polynomial | det(A - λI) |
| Sum of Eigenvalues | Trace(A) |
| Product of Eigenvalues | det(A) |
| Matrix Rank | Maximum linearly independent rows/columns |
| Symmetric Matrix | $A^T = A$ |
| Skew-Symmetric | $A^T = -A$ |
| Orthogonal | $A^T A = I$ |
| System Consistency | Compare rank(A) and rank([A\|B]) |

---

## Study Tips for IIT JEE

1. **Master the basics:** Know matrix types and operations thoroughly
2. **Practice determinant calculations:** Speed and accuracy are crucial
3. **Understand geometric interpretation:** Eigenvalues relate to transformation scaling
4. **Learn properties:** Many problems use properties instead of direct calculation
5. **Master system solving:** Know when solutions are unique, infinite, or none
6. **Practice previous year papers:** IIT repeats similar question patterns
7. **Time management:** Matrices questions can be solved quickly with practice
8. **Verify answers:** Always check your solution by substitution

---

**Last Updated:** May 2026
**Difficulty Level:** IIT JEE Advanced & Mains
**Total Concepts:** 50+
**Total Problems:** 10 solved examples
