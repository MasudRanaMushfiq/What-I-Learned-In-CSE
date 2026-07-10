

# Statistics For Engineers

### Course Information
**Course:** STAT 1211 (Statistics For Engineers)
**Course Type:** Theory, 2 Credit
**Prerequisite:** None

### Instructor
Dr. Provash Kumar Karmokar, Professor, Dept. of Statistics, University of Rajshahi

### Course Motivation
> To know basic theory of statistics and its applicability in real world situations.

---

## Course Contents

| Area | Topics Covered |
|---|---|
| **Descriptive Statistics** | Meaning and scope of statistics, Sources and types of statistical data, Representation of data, Location, Dispersion and their measures, Skewness, Kurtosis, Moments and Cumulants |
| **Probability** | Concept of probability, Sample Space, Events, Union and Intersection, Laws of probability, Conditional probabilities, Bayes' Theorem, Chebyshev's Inequality |
| **Random Variables & Distributions** | Discrete and continuous random variables, Density and distributional functions, Mathematical expectation, Joint/Marginal/Conditional functions, Moment and Cumulant generating functions, Binomial, Poisson, Normal, Bivariate Normal |
| **Regression and Correlation** | Correlation, Rank correlation, Partial and Multiple correlations, Linear Regression, Principle of Least Squares, Lines of best fit, Residual Analysis |
| **Test of Significance** | Null/Alternative hypothesis, Type-I/II errors, Level of significance, Single/Two sample tests for mean and variance, Chi-square test for 2×2 contingency tables, Independence test |

---

## Textbooks

**Primary Texts:**

1. A. J. B. Anderson — *Interpreting Data*, Chapman and Hall, London
2. H. Cramer — *The Elements of Probability Theory*, Wiley, New York

---

## Table of Contents

1. [Module I – Introduction to Statistics and Data Handling](#module-i)
2. [Module II – Descriptive Statistics (Univariate Analysis)](#module-ii)
3. [Module III – Foundations of Probability Theory](#module-iii)
4. [Module IV – Random Variables and Probability Distributions](#module-iv)
5. [Module V – Mathematical Expectation and Generating Functions](#module-v)
6. [Module VI – Theoretical Probability Distributions](#module-vi)
7. [Module VII – Bivariate Data Analysis (Correlation and Regression)](#module-vii)
8. [Module VIII – Inferential Statistics and Hypothesis Testing](#module-viii)

---

## Module I

## Introduction to Statistics and Data Handling

### 1.1 Definition and Scope

**Statistics** is the science of collecting, organizing, presenting, analyzing, and interpreting data to make scientific inferences and decisions.

> 💡 **CSE Relevance:** Statistics is the mathematical backbone of Data Science, Machine Learning, AI, and Network Analysis — all core areas of modern Computer Science and Engineering.

---

### 1.2 Applications in CSE

| Application Area | Role of Statistics |
|---|---|
| **Data Analysis** | Identifying patterns and trends in large datasets |
| **Machine Learning & AI** | Foundation for regression, classification, and predictive modelling |
| **Network Traffic Analysis** | Detecting traffic patterns, anomalies, and security threats |
| **Algorithm Efficiency** | Improving accuracy and efficiency of computational algorithms |

---

### 1.3 Types of Data

- **Primary Data** — Original data collected directly from the source (e.g., surveys, interviews, experiments)
- **Secondary Data** — Data collected by someone else for another purpose (e.g., books, government publications, databases)

---

### 1.4 Representation of Statistical Data

| Method | Type | Best Used For |
|---|---|---|
| **Frequency Distribution Table** | Tabular | Summarising large datasets |
| **Contingency Table** | Tabular | Showing relationships between two variables |
| **Bar Chart** | Graphical | Discrete or categorical data |
| **Pie Chart** | Graphical | Showing proportions of a whole |
| **Histogram** | Graphical | Continuous data grouped into intervals |
| **Frequency Polygon** | Graphical | Comparing frequency distributions |

---

## Module II

## Descriptive Statistics (Univariate Analysis)

### 2.1 Measures of Central Tendency

Single values describing the **centre** of a distribution:

| Measure | Formula / Description | Best Used When |
|---|---|---|
| **Arithmetic Mean (AM)** | Sum of all values ÷ number of observations | General-purpose; most stable measure |
| **Geometric Mean (GM)** | $n$-th root of the product of $n$ values | Exponential growth data (e.g., compound interest, population growth) |
| **Harmonic Mean (HM)** | Reciprocal of AM of reciprocals | Rates and ratios (e.g., average speed) |
| **Median** | Middle value when data is ordered | Skewed distributions; robust against outliers |
| **Mode** | Most frequently occurring value | Finding the most common/typical value |

> 💡 **Key Relationship:** For any set of positive numbers: **AM ≥ GM ≥ HM**

---

### 2.2 Measures of Dispersion

Quantifying the **spread** of data around the centre:

| Measure | Description |
|---|---|
| **Range** | Difference between maximum and minimum values |
| **Variance ($\sigma^2$)** | Average squared deviation from the mean |
| **Standard Deviation (SD, $\sigma$)** | Square root of variance; in the same units as the data |
| **Coefficient of Variation (CV)** | $(SD / Mean) \times 100\%$ — compares relative variability between different datasets |

> 💡 **Note:** CV is dimensionless, making it useful for comparing spread across datasets with different units or scales (e.g., comparing height variability vs. weight variability).

---

### 2.3 Moments

**Moments** are mathematical measures that describe the shape of a distribution:

| Moment | What It Measures |
|---|---|
| **1st Moment** | Mean (location) |
| **2nd Moment** | Variance (spread) |
| **3rd Moment** | Skewness (asymmetry) |
| **4th Moment** | Kurtosis (peakedness) |

**Cumulants** are an alternative set of descriptors closely related to moments, often used in advanced probability theory.

---

### 2.4 Skewness

**Skewness** measures the **asymmetry** of a distribution:

| Type | Tail Direction | Mean vs. Median |
|---|---|---|
| **Positive Skew** | Tail to the **right** | Mean > Median |
| **Negative Skew** | Tail to the **left** | Mean < Median |
| **Zero (Symmetric)** | No tail (balanced) | Mean = Median |

---

### 2.5 Kurtosis

**Kurtosis** measures the **peakedness** of a distribution:

| Type | Shape | Description |
|---|---|---|
| **Leptokurtic** | Thin, pointed peak | Heavier tails than normal |
| **Mesokurtic** | Normal bell curve | Baseline — same as Normal distribution |
| **Platykurtic** | Flat, broad peak | Lighter tails than normal |

---

## Module III

## Foundations of Probability Theory

### 3.1 Basic Concepts

| Term | Definition |
|---|---|
| **Random Experiment** | An experiment where the outcome is not unique but one of several possibilities |
| **Sample Space ($S$)** | The set of all possible outcomes of a random experiment |
| **Event** | A subset of the sample space |
| **Probability** | A measure from 0 to 1 of the likelihood of an event occurring |

> 💡 **Key Rule:** $P(S) = 1$ (the probability of the entire sample space is always 1)

---

### 3.2 Set Operations on Events

| Operation | Notation | Meaning |
|---|---|---|
| **Union** | $A \cup B$ | Either A or B (or both) occur |
| **Intersection** | $A \cap B$ | Both A and B occur |
| **Complement** | $A^c$ or $\bar{A}$ | A does NOT occur |

---

### 3.3 Laws of Probability

- **Addition Rule:** $P(A \cup B) = P(A) + P(B) - P(A \cap B)$
- **Multiplication Rule (Independent Events):** $P(A \cap B) = P(A) \cdot P(B)$
- **Conditional Probability:** $P(A \mid B) = \dfrac{P(A \cap B)}{P(B)}$

---

### 3.4 Bayes' Theorem

Used to **update** the probability of an event based on new evidence (conditional probabilities):

$$P(A_i \mid B) = \frac{P(B \mid A_i) \cdot P(A_i)}{\sum_{j} P(B \mid A_j) \cdot P(A_j)}$$

> 💡 **CSE Application:** Bayes' Theorem is the foundation of **Naive Bayes Classifiers** used in spam filtering, document classification, and medical diagnosis systems.

---

### 3.5 Chebyshev's Inequality

For **any** distribution with mean $\mu$ and standard deviation $\sigma$:

$$P(|X - \mu| \geq k\sigma) \leq \frac{1}{k^2}$$

- Provides an **upper bound** on the probability that a random variable deviates from its mean by more than $k$ standard deviations.
- Applies regardless of the shape of the distribution — no assumption needed.

---

## Module IV

## Random Variables and Probability Distributions

### 4.1 Random Variable (RV)

A **Random Variable** is a function that assigns a real number to each outcome of a random experiment.

| Type | Description | CSE Example |
|---|---|---|
| **Discrete RV** | Takes countable values | Number of bugs in a software build |
| **Continuous RV** | Takes infinite values in a range | CPU execution time; response latency |

---

### 4.2 Probability Functions

| Function | Symbol | Applies To | Description |
|---|---|---|---|
| **Probability Mass Function (PMF)** | $P(X = x)$ | Discrete RV | Gives exact probability for each value |
| **Probability Density Function (PDF)** | $f(x)$ | Continuous RV | Relative likelihood; area under curve = probability |
| **Cumulative Distribution Function (CDF)** | $F(x) = P(X \leq x)$ | Both | Probability that RV is less than or equal to a value |

> 💡 **Key Property:** For any valid PMF: $\sum P(X = x) = 1$. For any valid PDF: $\int_{-\infty}^{\infty} f(x)\,dx = 1$

---

### 4.3 Joint, Marginal and Conditional Distributions

For two random variables $X$ and $Y$:

| Concept | Description |
|---|---|
| **Joint Distribution** | $f(x, y)$ — describes the behaviour of both variables together |
| **Marginal Distribution** | Distribution of one variable, obtained by summing/integrating out the other |
| **Conditional Distribution** | Distribution of one variable given a fixed value of the other: $f(x \mid y)$ |
| **Conditional Expectation** | $E(X \mid Y = y)$ — expected value of $X$ given $Y$ |
| **Conditional Variance** | $\text{Var}(X \mid Y = y)$ — variance of $X$ given $Y$ |

---

## Module V

## Mathematical Expectation and Generating Functions

### 5.1 Mathematical Expectation

The **Expected Value** $E(X)$ is the long-term average (weighted mean) of a random variable:

- Discrete: $E(X) = \sum x \cdot P(X = x)$
- Continuous: $E(X) = \int_{-\infty}^{\infty} x \cdot f(x)\,dx$

**Key Properties:**
- $E(aX + b) = aE(X) + b$
- $E(X + Y) = E(X) + E(Y)$ (always true)

---

### 5.2 Variance

$$\text{Var}(X) = E(X^2) - [E(X)]^2$$

- Measures the **spread** of a distribution around its mean.
- $\text{Var}(aX + b) = a^2 \text{Var}(X)$

---

### 5.3 Generating Functions

| Function | Definition | Purpose |
|---|---|---|
| **Moment Generating Function (MGF)** | $M_X(t) = E(e^{tX})$ | Generates all moments; uniquely identifies a distribution |
| **Cumulant Generating Function (CGF)** | $\ln M_X(t)$ | Generates cumulants; simplifies calculations for independent RVs |
| **Characteristic Function** | $\phi_X(t) = E(e^{itX})$ | Always exists (unlike MGF); used in advanced probability theory |

> 💡 **How MGF works:** Differentiating $M_X(t)$ with respect to $t$ and setting $t = 0$ gives the moments: $E(X^n) = M_X^{(n)}(0)$

---

### 5.4 Covariance

**Covariance** measures the **directional relationship** between two random variables:

$$\text{Cov}(X, Y) = E(XY) - E(X) \cdot E(Y)$$

| Value | Meaning |
|---|---|
| **Positive** | X and Y tend to increase together |
| **Negative** | One increases as the other decreases |
| **Zero** | No linear relationship (may still be dependent) |

---

## Module VI

## Theoretical Probability Distributions

### 6.1 Discrete Distributions

| Distribution | Parameter(s) | Key Property | CSE Example |
|---|---|---|---|
| **Bernoulli** | $p$ (success probability) | Single trial; two outcomes (Success/Failure) | A single packet either arrives or is lost |
| **Binomial** | $n$, $p$ | Number of successes in $n$ independent Bernoulli trials; Mean = $np$, Var = $np(1-p)$ | Number of correct bits in an $n$-bit transmission |
| **Poisson** | $\lambda$ (rate) | Models rare events in a fixed interval; Mean = Variance = $\lambda$ | Number of server crashes per day; network requests per second |

> 💡 **Poisson Approximation:** The Binomial distribution approaches the Poisson distribution when $n$ is very large and $p$ is very small, with $\lambda = np$.

---

### 6.2 Continuous Distributions

#### Normal (Gaussian) Distribution

$$f(x) = \frac{1}{\sigma\sqrt{2\pi}} e^{-\frac{1}{2}\left(\frac{x-\mu}{\sigma}\right)^2}$$

- Symmetric **bell-shaped** curve defined by mean $\mu$ and standard deviation $\sigma$.
- The most important distribution in statistics due to the **Central Limit Theorem**.

| Property | Description |
|---|---|
| **Symmetry** | Mean = Median = Mode |
| **68-95-99.7 Rule** | ~68% of data within 1σ; ~95% within 2σ; ~99.7% within 3σ |
| **Standard Normal** | $Z = (X - \mu)/\sigma$; has mean 0 and variance 1 |

#### Bivariate Normal Distribution

- Joint distribution of **two normally distributed** variables $X$ and $Y$.
- Described by means $\mu_X$, $\mu_Y$; standard deviations $\sigma_X$, $\sigma_Y$; and correlation $\rho$.
- Key property: If $(X, Y)$ is bivariate normal and $\rho = 0$, then $X$ and $Y$ are **independent**.

> 💡 **Central Limit Theorem (CLT):** As sample size $n \to \infty$, the distribution of the sample mean approaches a Normal distribution — regardless of the original population's distribution. This is why the Normal distribution is so universally important.

---

## Module VII

## Bivariate Data Analysis — Correlation and Regression

### 7.1 Correlation Analysis

**Correlation** measures the **strength and direction** of the linear relationship between two variables.

| Method | Description | Range |
|---|---|---|
| **Pearson's Coefficient ($r$)** | Measures linear correlation between two continuous variables | −1 to +1 |
| **Rank Correlation (Spearman's $r_s$)** | Used when data is ranked or ordinal | −1 to +1 |
| **Partial Correlation** | Correlation between two variables after removing the effect of a third | −1 to +1 |
| **Multiple Correlation** | Correlation of one variable with a combination of several others | 0 to +1 |

| Value of $r$ | Interpretation |
|---|---|
| $+1$ | Perfect positive linear relationship |
| $0$ | No linear relationship |
| $-1$ | Perfect negative linear relationship |

> 💡 **Important:** Correlation does NOT imply causation. Two variables can be strongly correlated without one causing the other.

---

### 7.2 Scatter Diagram

A **visual plot** of paired $(x, y)$ data points used to:
- Identify the **direction** of the relationship (positive/negative)
- Estimate the **strength** of the relationship
- Detect **outliers** or **non-linear patterns**

---

### 7.3 Regression Analysis

**Regression** provides a **mathematical model** of the average relationship, used for **prediction**.

#### Simple Linear Regression

$$y = \beta_0 + \beta_1 x + \epsilon$$

| Term | Meaning |
|---|---|
| $y$ | Dependent variable (response) |
| $x$ | Independent variable (predictor) |
| $\beta_0$ | Intercept — value of $y$ when $x = 0$ |
| $\beta_1$ | Slope — change in $y$ per unit change in $x$ |
| $\epsilon$ | Random error term |

---

### 7.4 Principle of Least Squares

The **best-fit line** is found by minimising the **sum of squared residuals** (differences between observed and predicted values):

$$\text{Minimise} \sum_{i=1}^{n}(y_i - \hat{y}_i)^2$$

This yields the **normal equations** for estimating $\beta_0$ and $\beta_1$.

---

### 7.5 Residual Analysis

A **residual** is the difference between the observed value and the predicted value: $e_i = y_i - \hat{y}_i$

Residual analysis checks:
- Whether the model assumptions (linearity, constant variance, normality of errors) are satisfied
- Whether any patterns remain (suggesting a better model is needed)
- Identification of influential outliers

---

## Module VIII

## Inferential Statistics and Hypothesis Testing

### 8.1 Population vs. Sample

| Concept | Definition | Notation |
|---|---|---|
| **Population** | The entire group being studied | Parameter: $\mu$, $\sigma^2$ |
| **Sample** | A subset of the population used to make inferences | Statistic: $\bar{x}$, $s^2$ |

---

### 8.2 Hypothesis Testing Framework

A systematic procedure to test claims about a population:

| Step | Action |
|---|---|
| 1 | State the **Null Hypothesis ($H_0$)** — the default claim (no effect / no difference) |
| 2 | State the **Alternative Hypothesis ($H_1$)** — what you aim to prove |
| 3 | Choose the **Level of Significance ($\alpha$)** — typically 0.05 or 0.01 |
| 4 | Select the appropriate **test statistic** |
| 5 | Define **Acceptance** and **Rejection Regions** using degrees of freedom |
| 6 | Compute the test statistic from sample data |
| 7 | **Decision:** Reject $H_0$ if test statistic falls in the rejection region |

---

### 8.3 Types of Errors

| Error Type | Description | Analogy |
|---|---|---|
| **Type-I Error ($\alpha$)** | Rejecting $H_0$ when it is actually **true** | False Positive |
| **Type-II Error ($\beta$)** | Failing to reject $H_0$ when it is actually **false** | False Negative |

> 💡 **Trade-off:** Decreasing $\alpha$ (reducing Type-I error) generally increases $\beta$ (Type-II error), and vice versa. The goal is to balance both in practice.

---

### 8.4 Common Statistical Tests

| Test | Sample Size | Condition | Used For |
|---|---|---|---|
| **z-test** | Large ($n > 30$) | Known population variance or large $n$ | Testing means or proportions |
| **t-test** | Small ($n \leq 30$) | Unknown population variance | Comparing one or two sample means |
| **F-test** | Any | Comparing variances | Testing equality of two population variances |
| **Chi-Square ($\chi^2$)** | Any | Categorical data | Independence test in 2×2 contingency tables |

---

### 8.5 Degrees of Freedom

**Degrees of Freedom (df)** — the number of independent pieces of information available to estimate a parameter.

- One-sample t-test: $df = n - 1$
- Two-sample t-test: $df = n_1 + n_2 - 2$
- Chi-square test: $df = (r-1)(c-1)$ for an $r \times c$ table

---

### 8.6 Chi-Square Test for Independence (2×2 Table)

Used to test whether two categorical variables are **independent** of each other.

$$\chi^2 = \sum \frac{(O - E)^2}{E}$$

where $O$ = observed frequency and $E$ = expected frequency.

- **Decision:** Reject $H_0$ (independence) if $\chi^2_{\text{calc}} > \chi^2_{\text{critical}}$ at the chosen $\alpha$.

---

## Quick Reference Summary

| Module | Core Concept | Key Terms |
|---|---|---|
| I | Statistics fundamentals and data types | Primary/Secondary data, Histogram, Frequency Table |
| II | Descriptive measures | AM, GM, HM, Variance, SD, CV, Skewness, Kurtosis |
| III | Probability theory | Sample Space, Bayes' Theorem, Chebyshev's Inequality |
| IV | Random variables | PMF, PDF, CDF, Discrete/Continuous RV, Joint Distribution |
| V | Expectation and generating functions | $E(X)$, Var$(X)$, MGF, Covariance |
| VI | Standard distributions | Binomial, Poisson, Normal, Bivariate Normal, CLT |
| VII | Correlation and regression | Pearson's $r$, Least Squares, Residual Analysis |
| VIII | Hypothesis testing | $H_0$, $H_1$, Type-I/II Error, z-test, t-test, $\chi^2$ |

---
*STAT 1211 — Statistics and Probability Theory | Dept. of CSE, University of Rajshahi*





