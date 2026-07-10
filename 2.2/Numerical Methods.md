

# Numerical Methods

### Course Information
**Course:** MATH 2231 (Numerical Methods)
**Course Type:** Theory, 2 Credits
**Prerequisite:** CSE 1121 (Structural Programming Language)

### Instructor
Dr. Somlal Das, Professor, Dept. of CSE, University of Rajshahi 

### Course Motivation
> To know the story of how functions, derivatives, integrals, and differential equations are handled as strings of numbers in the computer.

---

## Course Contents

| Area | Topics Covered |
| --- | --- |
| **Approximations and Errors** | Accuracy and Precision, Error Definitions, Round-Off Errors, Truncation Errors |
| **Roots of Equations** | Graphical Methods, Bisection Method, False-Position Method, Simple One-Point Iteration, Newton-Raphson Method, Secant Method |
| **Systems of Linear Algebraic Equations** | Gauss Elimination, Naive Gauss Elimination, Pitfalls of Elimination Methods, Matrix Inversion, Gauss-Seidel, Error Analysis and System Condition |
| **Curve Fitting** | Linear Regression, Polynomial Regression, Multiple Linear Regression, Newton's Divided-Difference Interpolating Polynomials, Lagrange Interpolating Polynomials, Coefficients of an Interpolating Polynomial, Curve Fitting with Sinusoidal Functions |
| **Numerical Differentiation and Integration** | Trapezoidal Rule, Simpson's Rules, Integration with Unequal Segments, Romberg Integration, Gauss Quadrature, High-Accuracy Differentiation Formulas, Richardson Extrapolation, Derivatives of Unequally Spaced Data |
| **Additional Topics** | Pseudorandom-Number Generators, The FFT |

---

## Textbooks

**Primary Texts:**
1. Steven C. Chapra, Raymond P. Canale — *Numerical Methods for Engineers*, McGraw-Hill

---

## Table of Contents

1. [Chapter 1 – Introduction to Numerical Methods](#chapter-1)
2. [Chapter 2 – Approximations and Errors](#chapter-2)
3. [Chapter 3 – Roots of Equations](#chapter-3)
4. [Chapter 4 – Systems of Linear Algebraic Equations](#chapter-4)
5. [Chapter 5 – Curve Fitting and Interpolation](#chapter-5)
6. [Chapter 6 – Numerical Differentiation and Integration](#chapter-6)
7. [Chapter 7 – Ordinary Differential Equations](#chapter-7)
8. [Chapter 8 – Pseudorandom-Number Generators and the FFT](#chapter-8)

---

## Chapter 1
## Introduction to Numerical Methods

### 1.1 Definition and Motivation

**Numerical Methods:** Mathematical techniques formulated so that problems can be solved using basic arithmetic operations — addition, subtraction, multiplication, and division. These methods are essential for solving complex engineering problems that lack analytical (exact) solutions, such as non-linear models or those involving complicated geometries.

---

### 1.2 Steps in Solving Practical Problems

Solving a practical engineering problem using numerical methods follows a structured process:

| Step | Action |
|---|---|
| **1** | **State the problem clearly**, including any simplifying assumptions |
| **2** | **Develop a mathematical statement** (model) that can be solved for a numerical answer |
| **3** | **Solve the equations** using an appropriate numerical algorithm |
| **4** | **Interpret the result** to arrive at a decision |

> 📌 Numerical methods do not produce exact symbolic answers — they produce **approximate numerical solutions** that are close enough to the true answer for practical engineering purposes. The quality of the approximation depends on the method chosen and the care taken to control errors.

---

## Chapter 2
## Approximations and Errors

### 2.1 Accuracy, Precision, and Numerical Error

**Numerical error** is the difference between the exact mathematical solution and the approximate numerical solution.

- **Accuracy** refers to how close a computed value is to the true value.
- **Precision** refers to how consistently repeated computations yield the same result, regardless of whether that result is close to the true value.

> 📌 A result can be **precise but not accurate** (consistently wrong) or **accurate but not precise** (correct on average but with large variation). In numerical methods, both accuracy and precision must be managed carefully.

---

### 2.2 Types of Errors

| Error Type | Cause | Example |
|---|---|---|
| **Inherent Error** | Errors existing in the problem itself, often due to approximations in given data or limitations of measuring instruments | Imprecise physical measurements used as input |
| **Round-Off Error** | Results from the computer's inability to represent exact numbers due to limited significant figures | Storing $1/3$ as $0.3333333$ |
| **Truncation Error** | Results from using an approximate formula in place of an exact mathematical procedure, such as stopping an infinite series after a few terms | Approximating $e^x$ by the first three terms of its Taylor series |
| **Blunders** | Errors caused by human imperfection, such as wrong assumptions or mistakes in computer programming | Incorrect loop bounds in code |

---

### 2.3 Measuring Errors

Let $x$ be the true value and $\bar{x}$ be the approximate value. The following error measures are defined:

**Absolute Error ($E_A$):** The numerical difference between the true and approximate values:

$$E_A = |x - \bar{x}|$$

**Relative Error ($E_R$):** The absolute error divided by the true value:

$$E_R = \frac{E_A}{x}$$

**Percentage Error ($E_p$):** The relative error expressed as a percentage:

$$E_p = E_R \times 100\%$$

---

### 2.4 Significant Figures

Significant figures are the digits that can be used with confidence. The rules for identifying significant figures are:

- All **non-zero digits** are significant.
- **Zeros between non-zero digits** are significant.
- **Leading zeros** are not significant.

> 💡 The number of significant figures directly determines the precision of the result. When performing a sequence of calculations, round-off errors can accumulate — a phenomenon that must be carefully managed in numerical algorithms.

---

### 2.5 Round-Off Errors

Round-off error results from the computer's inability to represent exact numbers due to limited significant figures. Because computers store numbers in binary floating-point format with a fixed number of bits, many decimal fractions cannot be represented exactly. This limitation introduces small errors in every arithmetic operation, which can compound over many calculations.

---

### 2.6 Truncation Errors

Truncation error results from using an approximate formula in place of an exact mathematical procedure, such as stopping an infinite series after a few terms. The **Taylor Series** is the foundation for understanding and quantifying truncation error in numerical differentiation and ODE methods:

$$f(x_{i+1}) = f(x_i) + f'(x_i)h + \frac{f''(x_i)}{2!}h^2 + \frac{f'''(x_i)}{3!}h^3 + \cdots$$

where $h$ is the step size. Truncating this series after the first-derivative term gives the basis of Euler's method; the discarded terms represent the truncation error.

---

## Chapter 3
## Roots of Equations

### 3.1 Overview

Finding roots means solving $f(x) = 0$ — that is, finding the value of $x$ for which the function equals zero. Methods are categorized into **Bracketing** methods (always convergent) and **Open** methods (faster but may diverge).

---

### 3.2 Graphical Methods

Before applying a numerical algorithm, plotting $f(x)$ provides an initial visual estimate of where roots lie. Graphical methods reveal how many roots exist and roughly where they are, which helps in choosing good starting values for more precise methods.

> 📌 Graphical methods are not used for precise answers but are valuable as a **first diagnostic step** to understand the behavior of the function and identify appropriate initial guesses.

---

### 3.3 Bracketing Methods (Always Convergent)

Bracketing methods require two initial guesses $a$ and $b$ that "bracket" the root — that is, $f(a)$ and $f(b)$ must have opposite signs, guaranteeing by the Intermediate Value Theorem that at least one root lies in $[a, b]$.

#### Bisection Method

Repeatedly halves the interval $[a, b]$ where the root lies.

- The midpoint $x_r = (a + b)/2$ is computed at each step.
- If $f(a) \cdot f(x_r) < 0$, the root lies in $[a, x_r]$; otherwise it lies in $[x_r, b]$.
- It is **reliable** but converges **slowly** (linearly — one bit of accuracy per iteration).

#### False Position Method (Regula Falsi)

Connects points $(a,\, f(a))$ and $(b,\, f(b))$ with a straight line; the intersection of that line with the x-axis is the next approximation:

$$x_r = b - \frac{f(b)(a - b)}{f(a) - f(b)}$$

- Uses the shape of the function (not just the midpoint) to make smarter guesses.
- Converges faster than bisection in most cases, while retaining the bracketing guarantee.

| Method | Convergence | Starting Requirement |
|---|---|---|
| **Bisection** | Linear (slow but guaranteed) | Two points bracketing the root |
| **False Position** | Faster than bisection | Two points bracketing the root |

---

### 3.4 Open Methods (Faster but May Diverge)

Open methods require only one or two starting points that do not need to bracket the root. They converge much faster when they do converge, but they can diverge if the starting point is poorly chosen.

#### Simple One-Point Iteration (Fixed-Point Iteration)

Rearranges $f(x) = 0$ into the form $x = g(x)$ and iterates:

$$x_{n+1} = g(x_n)$$

Convergence depends on $|g'(x)| < 1$ near the root.

#### Newton-Raphson Method

Uses the slope (derivative) at a point to find the next guess:

$$x_{n+1} = x_n - \frac{f(x_n)}{f'(x_n)}$$

- It is **highly efficient** due to **quadratic convergence** — the number of accurate digits roughly doubles each iteration.
- *Example (CSE):* Used in high-speed digital computer programs for finding square roots or solving transcendental equations like $x e^x - 1 = 0$.

#### Secant Method

Similar to Newton-Raphson but **approximates the derivative** using two previous points instead of computing it analytically:

$$x_{n+1} = x_n - \frac{f(x_n)(x_{n-1} - x_n)}{f(x_{n-1}) - f(x_n)}$$

- Does not require an explicit formula for $f'(x)$.
- Converges faster than bisection but slightly slower than Newton-Raphson.

| Method | Convergence Rate | Derivative Required |
|---|---|---|
| **Simple Iteration** | Linear (conditional) | No |
| **Newton-Raphson** | Quadratic | Yes — $f'(x)$ |
| **Secant** | Superlinear (~1.62) | No — approximated from two points |

---

## Chapter 4
## Systems of Linear Algebraic Equations

### 4.1 Overview

Many engineering problems reduce to solving a system of $n$ linear equations in $n$ unknowns, represented in matrix form as $[A]\{x\} = \{b\}$. Solution methods fall into **Direct** and **Iterative** categories.

---

### 4.2 Solving Small Numbers of Equations

For very small systems (2 or 3 equations), direct algebraic substitution or Cramer's Rule may be applied. For larger systems, systematic algorithms are required.

---

### 4.3 Gauss Elimination

**Naive Gauss Elimination** transforms the augmented matrix $[A|b]$ into **upper triangular form** through forward elimination, then recovers the unknowns via **back-substitution**.

**Forward Elimination:** For each pivot row $k$, eliminate the variable $x_k$ from all rows below it:

$$a_{ij} \leftarrow a_{ij} - \frac{a_{ik}}{a_{kk}} \cdot a_{kj}$$

**Back-Substitution:** Solve for unknowns starting from the last equation and working upward:

$$x_i = \frac{b_i - \sum_{j=i+1}^{n} a_{ij} x_j}{a_{ii}}$$

---

### 4.4 Pitfalls of Elimination Methods

| Pitfall | Description |
|---|---|
| **Division by Zero** | Occurs if a pivot element $a_{kk} = 0$; remedied by **partial pivoting** (row swapping) |
| **Round-Off Error Accumulation** | Large numbers of operations amplify floating-point errors; pivoting also mitigates this |
| **Ill-Conditioned Systems** | Small changes in coefficients cause large changes in the solution; diagnosed by the **condition number** |

> 📌 **Partial pivoting** — swapping rows so that the largest absolute value in a column becomes the pivot — reduces both the division-by-zero problem and round-off error accumulation.

---

### 4.5 LU Decomposition and Matrix Inversion

**LU Decomposition** factorizes the coefficient matrix into a **Lower triangular matrix (L)** and an **Upper triangular matrix (U)** such that $[A] = [L][U]$.

- Solving $[A]\{x\} = \{b\}$ then reduces to two triangular systems: $[L]\{d\} = \{b\}$ (forward substitution) and $[U]\{x\} = \{d\}$ (back-substitution).
- LU Decomposition is **preferred for calculating matrix inverses**, because once $[L]$ and $[U]$ are computed, multiple right-hand sides can be solved efficiently.

**The Matrix Inverse:** The inverse $[A]^{-1}$ is computed by solving $[A][X] = [I]$ column by column using LU Decomposition, where $[I]$ is the identity matrix.

---

### 4.6 Gauss-Seidel Iterative Method

An **iterative technique** where the most recently computed values are used immediately in the next calculation to speed up convergence. For the $i$-th equation:

$$x_i^{(k+1)} = \frac{1}{a_{ii}}\left(b_i - \sum_{j<i} a_{ij} x_j^{(k+1)} - \sum_{j>i} a_{ij} x_j^{(k)}\right)$$

**Convergence Condition:** Convergence is guaranteed if the system is **diagonally dominant** — the absolute value of the diagonal element is greater than the sum of the absolute values of all other elements in that row:

$$|a_{ii}| > \sum_{j \neq i} |a_{ij}|$$

---

### 4.7 Error Analysis and System Condition

The **condition number** of a matrix measures sensitivity to perturbations. A high condition number indicates an **ill-conditioned system** where small errors in the data or round-off errors in computation can lead to large errors in the solution. Error analysis evaluates whether the computed solution is trustworthy given the precision of the input data.

---

## Chapter 5
## Curve Fitting and Interpolation

### 5.1 Overview

Curve fitting and interpolation are techniques for representing discrete data mathematically. **Regression** fits a smooth curve that does not necessarily pass through every data point (used when data contains noise), while **interpolation** finds a curve that passes exactly through every data point.

---

### 5.2 Least Squares Regression

#### Linear Regression

**Least Squares Regression** minimizes the sum of the squares of the vertical deviations between each data point and the fitted curve. For a straight line $y = a_0 + a_1 x$, the normal equations yield:

$$a_1 = \frac{n\sum x_i y_i - \sum x_i \sum y_i}{n\sum x_i^2 - (\sum x_i)^2}, \qquad a_0 = \bar{y} - a_1 \bar{x}$$

- *Example (CSE):* Used in **data smoothing** where experimental data contains errors, helping to predict the general trend rather than passing exactly through every noisy point.

#### Polynomial Regression

Fits a polynomial of degree $m$ to data using least squares. The model is $y = a_0 + a_1 x + a_2 x^2 + \cdots + a_m x^m$, and the coefficients are found by solving a system of normal equations.

#### Multiple Linear Regression

Extends linear regression to problems with **more than one independent variable**: $y = a_0 + a_1 x_1 + a_2 x_2 + \cdots + a_k x_k$. The coefficients are determined using matrix least squares methods.

#### Curve Fitting with Sinusoidal Functions

Fits a sinusoidal (harmonic) model to periodic data. The general form is:

$$y = A_0 + C_1 \cos(\omega x) + D_1 \sin(\omega x)$$

This is the basis of **Fourier analysis** and is closely related to the FFT (see Chapter 8).

---

### 5.3 Interpolation

Used to find intermediate values between tabulated data points, under the assumption that the data is exact (no noise).

#### Newton's Divided-Difference Interpolating Polynomials

A general interpolation formula valid for **unequally spaced** data. The polynomial is built incrementally using divided differences:

$$f_n(x) = b_0 + b_1(x - x_0) + b_2(x - x_0)(x - x_1) + \cdots$$

where $b_0, b_1, b_2, \ldots$ are the divided differences computed from the data table.

**Newton's Forward/Backward Difference Interpolation** is a special case used for **equally spaced** data points, where the divided differences simplify to finite differences.

#### Lagrange Interpolating Polynomials

A general formula that does not require computing divided differences. For $n+1$ data points:

$$f_n(x) = \sum_{i=0}^{n} L_i(x)\, f(x_i), \quad \text{where } L_i(x) = \prod_{\substack{j=0 \\ j \neq i}}^{n} \frac{x - x_j}{x_i - x_j}$$

Used when data points are **not equally spaced** and a clean closed-form expression is preferred.

#### Coefficients of an Interpolating Polynomial

Both Newton's and Lagrange methods produce the same unique interpolating polynomial of degree $\leq n$ through $n+1$ points. The coefficients can also be found by solving a **Vandermonde system** of linear equations, though this approach is computationally expensive for large $n$.

#### Cubic Splines

Fits **low-order polynomials** between adjacent data points to ensure a **smooth curve** across the entire data range. Unlike a single high-degree polynomial, cubic splines avoid oscillation (Runge's phenomenon) and guarantee continuity of the function and its first two derivatives at every interior data point.

> 💡 **Cubic Splines** are preferred over high-degree interpolating polynomials for large datasets because they avoid oscillatory behavior and produce visually smooth, physically realistic curves.

---

## Chapter 6
## Numerical Differentiation and Integration

### 6.1 Numerical Differentiation

Calculates derivatives from discrete data points using the **Taylor Series**. Common finite-difference formulas:

| Formula | Expression | Error Order |
|---|---|---|
| **Forward Difference** | $f'(x_i) \approx \dfrac{f(x_{i+1}) - f(x_i)}{h}$ | $O(h)$ |
| **Backward Difference** | $f'(x_i) \approx \dfrac{f(x_i) - f(x_{i-1})}{h}$ | $O(h)$ |
| **Centered Difference** | $f'(x_i) \approx \dfrac{f(x_{i+1}) - f(x_{i-1})}{2h}$ | $O(h^2)$ |

> 📌 **Note:** Differentiation is **sensitive to data errors** and should be used with caution compared to integration. Small errors in $f(x)$ values are amplified when differences are taken, especially with small step sizes.

#### High-Accuracy Differentiation Formulas

Higher-order accuracy can be achieved by including more terms of the Taylor series. For example, the **higher-accuracy forward difference** for the first derivative uses additional data points to achieve $O(h^2)$ accuracy without requiring centered data.

#### Richardson Extrapolation

A powerful technique for improving the accuracy of any finite-difference approximation by combining two estimates computed at different step sizes $h$ and $h/2$:

$$D_{\text{accurate}} \approx \frac{4 D(h/2) - D(h)}{3}$$

This eliminates the leading error term and dramatically improves accuracy at no additional function evaluations.

#### Derivatives of Unequally Spaced Data

When data points are not uniformly spaced, standard finite-difference formulas cannot be applied directly. Instead, derivatives are estimated using **Lagrange interpolating polynomials** fitted to nearby data points, then differentiated analytically.

---

### 6.2 Numerical Integration (Quadrature)

Determines the area under a curve $\int_a^b f(x)\, dx$ when an analytical antiderivative is unavailable or impractical.

#### Trapezoidal Rule

Approximates the area under $f(x)$ between two points as a **trapezoid**:

$$\int_a^b f(x)\, dx \approx (b - a)\frac{f(a) + f(b)}{2}$$

- Accurate for **linear functions**; error is $O(h^2)$.
- The **composite Trapezoidal Rule** divides $[a, b]$ into $n$ equal segments and sums the areas of all trapezoids.

#### Simpson's 1/3 Rule

Uses a **quadratic polynomial** to fit three equally spaced points, providing higher accuracy than the Trapezoidal Rule:

$$\int_{x_0}^{x_2} f(x)\, dx \approx \frac{h}{3}\left[f(x_0) + 4f(x_1) + f(x_2)\right]$$

Error is $O(h^4)$ — significantly better than the Trapezoidal Rule.

#### Simpson's 3/8 Rule

Fits a **cubic polynomial** to four equally spaced points:

$$\int_{x_0}^{x_3} f(x)\, dx \approx \frac{3h}{8}\left[f(x_0) + 3f(x_1) + 3f(x_2) + f(x_3)\right]$$

Useful when the number of intervals is a multiple of 3.

| Rule | Polynomial Fit | Points Used | Error Order |
|---|---|---|---|
| **Trapezoidal** | Linear | 2 | $O(h^2)$ |
| **Simpson's 1/3** | Quadratic | 3 | $O(h^4)$ |
| **Simpson's 3/8** | Cubic | 4 | $O(h^4)$ |

#### Integration with Unequal Segments

When data points are **not equally spaced**, the Trapezoidal Rule can still be applied to each individual segment using its actual width, then summed. Simpson's rules require equal spacing and cannot be applied directly to unequal segments without adaptation.

#### Romberg Integration

An iterative technique that uses **Richardson's extrapolation** applied to the Trapezoidal Rule to provide **highly accurate estimates** with fewer function evaluations. It builds a triangular table of estimates, combining successive results to cancel error terms:

$$I = \frac{4I_{j,k-1} - I_{j-1,k-1}}{3}$$

> 💡 **Romberg Integration** is particularly efficient because it achieves high accuracy by reusing previously computed function values and extrapolating — avoiding the need to evaluate $f(x)$ at many new points.

#### Gauss Quadrature

Rather than using equally spaced points, **Gauss Quadrature** selects both the evaluation points (Gauss points) and the weights optimally to maximize accuracy for a given number of function evaluations:

$$\int_{-1}^{1} f(x)\, dx \approx \sum_{i=1}^{n} w_i f(x_i)$$

A $n$-point Gauss quadrature formula is exact for polynomials of degree up to $2n - 1$ — far more efficient than Newton-Cotes formulas (Trapezoidal, Simpson's) for smooth functions.

---

## Chapter 7
## Ordinary Differential Equations

### 7.1 Overview

Numerical methods solve **initial-value problems** (IVPs) of the form $dy/dx = f(x, y)$, $y(x_0) = y_0$, by stepping forward in time (or along the independent variable) from the known initial condition.

---

### 7.2 Euler's Method

The simplest one-step method. It uses the **slope at the beginning of the interval** to project to the next point:

$$y_{i+1} = y_i + f(x_i, y_i) \cdot h$$

- Easy to program and understand.
- Has **high truncation error** — $O(h^2)$ per step, $O(h)$ globally.
- The error can be reduced by decreasing the step size $h$, at the cost of more computation.

> 📌 **Euler's Method** is the first-order Taylor series approximation of the solution. Its simplicity makes it ideal for introducing ODE solvers, but in practice it is rarely used alone due to its large truncation error.


---


## Quick Reference Summary

| Chapter | Core Topic | Key Terms |
|---|---|---|
| 1 | Introduction | Numerical Methods, Arithmetic Operations, Problem-Solving Steps |
| 2 | Approximations and Errors | Accuracy, Precision, $E_A$, $E_R$, $E_p$, Round-Off, Truncation, Blunders, Significant Figures |
| 3 | Roots of Equations | Graphical, Bisection, False Position, Simple Iteration, Newton-Raphson $x_{n+1} = x_n - f/f'$, Secant |
| 4 | Linear Systems | Gauss Elimination, Back-Substitution, LU Decomposition, Matrix Inverse, Gauss-Seidel, Diagonal Dominance |
| 5 | Curve Fitting | Linear/Polynomial/Multiple Regression, Least Squares, Newton's Divided-Difference, Lagrange, Cubic Splines, Sinusoidal Fitting |
| 6 | Differentiation and Integration | Forward/Backward/Centered Differences, Richardson Extrapolation, Trapezoidal, Simpson's 1/3 and 3/8, Romberg, Gauss Quadrature |
| 7 | ODEs | Euler's Method, RK4 ($k_1$–$k_4$), Adaptive RK, Initial-Value Problems |
| 8 | PRNG and FFT | Linear Congruential Generator, DFT, FFT $O(N \log N)$, Spectral Analysis |

---
*MATH 2231 — Numerical Methods | Dept. of CSE, University of Rajshahi*






