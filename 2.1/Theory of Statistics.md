

# Theory of Statistics

### Course Information
**Course:** STAT-2111 (Theory of Statistics)
**Course Type:** Theory, 2 Credit
**Prerequisite:** STAT1211 Statistics for Engineers
### Instructor
Dr. M. Aminul Haque, Professor, Dept. of Statistics, University of Rajshahi

### Course Motivation
> To introduce students with statistical and probabilistic study of real life problems.

---

## Course Contents

| Area | Topics Covered |
| --- | --- |
| **Sampling Distributions** | Fisher’s Lemma. Study of Chi² Distribution, T-Distribution and F-Distribution, Properties, uses & Applications. Distribution of sample correlation coefficient in the null case. Sampling Distribution of the Medians and Range. |
| **Elements of Point Estimation** | Basic Concepts. Consistent estimates. Unbiased estimates. Mean and variance of estimates. Ideas of Efficiency. Principle of Maximum Likelihood. Illustration from Binomial, Poisson & Normal Distributions. |
| **Test of Significance** | Basic ideas of Null hypothesis. Alternative hypothesis. Type-I error, Type-II error, level of significance, Degree of freedom, Rejection region and Acceptance region. Test of Single mean, Single variance, Two sample means and variances. Test for 2x2 contingency tables. Independence test and practical examples. |
| **Decision Rules** | Statistical decisions; Statistical hypothesis; Critical region, Best critical region; Two types of errors; procedure of Test of hypothesis; Most powerful test, standard Errors. |
| **Advanced Hypothesis Testing** | Test of single mean & single variance. Comparison of two sample Means, proportions and Variances. Bartlett’s test for homogeneity of variances. Test for correlation and Regression coefficients. Exact test for 2x2 tables. Test for rc tables. Three-Way contingency tables. Large Sample Test of Significance. Non-parametric Test, One Sample and two Sample Sign Test. Run Test and Rank Sum Test. |


## Textbooks

**Primary Texts:**
1. Mood, Graybill and Boes — *Introduction to the Theory of Statistics*, McGraw-Hill, N. Y.

---

## Table of Contents

1. [Chapter 1 – Foundational Concepts](#chapter-1)
2. [Chapter 2 – Theory of Estimation](#chapter-2)
3. [Chapter 3 – Sampling Distributions](#chapter-3)
4. [Chapter 4 – Statistical Hypothesis Testing](#chapter-4)
5. [Chapter 5 – Decision Rules](#chapter-5)
6. [Chapter 6 – Analysis of Categorical Data](#chapter-6)
7. [Chapter 7 – Non-Parametric Tests](#chapter-7)

---

## Chapter 1
## Foundational Concepts

### 1.1 Fundamental Definitions

- **Population:** The complete collection of all outcomes, responses, measurements, or counts that are of interest.
- **Sample:** A subset or a representative part of a population.
- **Parameter:** A numerical value that describes a characteristic of an entire population, typically denoted by Greek letters (e.g., population mean $\mu$, variance $\sigma^2$).
- **Statistic:** A numerical value calculated from sample data used to describe characteristics of that sample (e.g., sample mean $\bar{x}$, sample variance $s^2$).

---

## Chapter 2
## Theory of Estimation

Estimation is the process of making inferences about population parameters based on information obtained from a sample.

### 2.1 Key Definitions

- **Estimator:** A rule or formula (usually a function of sample observations) used to calculate an estimate (e.g., the formula for the sample mean).
- **Estimate:** A specific numerical value obtained by applying an estimator to a particular sample (e.g., a calculated mean of 165 cm).
- **Point Estimate:** A single numerical value used to estimate a population parameter.
- **Interval Estimate:** A range of values within which the population parameter is expected to lie.

### 2.2 Basic Concepts of Point Estimation

**Elements of Point Estimations:** Basic Concepts.

### 2.3 Criteria for a Good Estimator

1.  **Unbiasedness (Unbiased estimates):** An estimator is unbiased if its expected value equals the true population parameter. For example, the sample mean $\bar{x}$ is an unbiased estimator of $\mu$.
2.  **Consistency (Consistent estimates):** An estimator is consistent if it converges in probability to the true parameter value as the sample size $n$ increases toward infinity.
3.  **Efficiency (Ideas of Efficiency):** Among a set of consistent/unbiased estimators, the one with the smallest variance is considered the most efficient. Mean and variance of estimates.
4.  **Sufficiency:** An estimator is sufficient if it contains all the information from the sample relevant to estimating the parameter.

### 2.4 Methods of Estimation

- **Maximum Likelihood Estimation (MLE) (Principle of Maximum Likelihood):** A method that finds parameter values maximizing the likelihood function, making the observed data as probable as possible.
- **Illustration from Binomial, Poisson & Normal Distributions:** The Principle of Maximum Likelihood is illustrated using the Binomial, Poisson, and Normal Distributions.
- **Other Methods:** Include the Method of Moments, Least Squares, and Bayesian Estimation.

---

## Chapter 3
## Sampling Distributions

**Sampling Distributing:** Fisher’s Lemma. Distribution of sample correlation coefficient in the null case. Sampling Distribution of the Medians and Range.

### 3.1 Chi-Square ($\chi^2$) Distribution

**Study of Chi² Distribution:**
- **Definition:** The distribution of the sum of squares of $n$ independent standard normal variates.
- **Properties:** It is a continuous, non-negative distribution that is positively skewed. Its mean equals its degrees of freedom ($k$), and its variance is $2k$.
- **Uses & Applications:** Used for testing population variance, goodness of fit, and independence of attributes in contingency tables.

### 3.2 Student’s t-Distribution

**Study of T-Distribution:**
- **Definition:** Arises when estimating the mean of a normally distributed population when the sample size is small ($n < 30$) and the population variance is unknown.
- **Properties:** Bell-shaped and symmetrical about zero, similar to the normal distribution but with heavier tails. As degrees of freedom increase, it approaches the standard normal distribution.
- **Uses & Applications:** Used for testing hypotheses about single means or the difference between two means.

### 3.3 F-Distribution

**Study of F-Distribution:**
- **Definition:** Defined as the ratio of two independent chi-square variates, each divided by its respective degrees of freedom.
- **Properties:** Continuous, non-negative, and positively skewed.
- **Uses & Applications:** Primarily used in Analysis of Variance (ANOVA) and for testing the equality of two population variances.

---

## Chapter 4
## Statistical Hypothesis Testing

### 4.1 Basic Ideas

**Test of Significance:**
- **Null Hypothesis ($H_0$):** The default assumption that there is no effect or no difference (e.g., a new drug is no better than a placebo). (Basic ideas of Null hypothesis).
- **Alternative Hypothesis ($H_1$ or $H_a$):** The claim we seek to support, contradicting the null hypothesis. (Basic ideas of Alternative hypothesis).
- **Level of Significance ($\alpha$):** The predefined threshold for the probability of rejecting a true null hypothesis (commonly 0.05 or 5%). (level of significance).
- **Degree of freedom:** A concept used in various statistical distributions (e.g., chi-square, t, F) representing the number of independent pieces of information available for estimating a parameter. (Degree of freedom).
- **Rejection region and Acceptance region:** The set of all values of the test statistic that lead to the rejection of the null hypothesis is the Rejection region (Critical Region). The set of values that leads to not rejecting the null hypothesis is the Acceptance region.
- **Critical Region:** The set of all values of the test statistic that lead to the rejection of the null hypothesis.
- **P-value:** The probability of obtaining a result at least as extreme as the observed one, assuming $H_0$ is true.

### 4.2 Errors in Testing

- **Type I Error:** Rejecting a true null hypothesis ("false positive"). (Type-I error).
- **Type II Error:** Failing to reject a false null hypothesis ("false negative"). (Type-II error).
- **Power of a Test:** The probability of correctly rejecting a false null hypothesis ($1 - \beta$).

---

## Chapter 5
## Decision Rules

### 5.1 Statistical Decisions and Hypothesis Testing

**Decision Rules:**
- **Statistical decisions:** Decisions made based on the outcome of a statistical test.
- **Statistical hypothesis:** An assertion or conjecture about the probability distribution of a population (e.g., the mean is 50).
- **Critical region, Best critical region:** The set of all values of the test statistic that lead to the rejection of the null hypothesis is the Critical region. The Best critical region is the critical region that maximizes the power of the test for a given significance level.
- **Two types of errors:** Type I Error (rejecting a true $H_0$) and Type II Error (failing to reject a false $H_0$).
- **Procedure of Test of hypothesis:** A systematic method including: 1) stating $H_0$ and $H_a$, 2) choosing a test statistic, 3) setting $\alpha$, 4) defining the critical region, 5) computing the test statistic, and 6) making a decision.
- **Most powerful test:** A test that has the greatest power among all tests of the same significance level for testing a simple hypothesis against a simple alternative.
- **Standard Errors:** The standard deviation of a sampling distribution of a statistic.

---

## Chapter 6
## Analysis of Categorical Data

### 6.1 Contingency Tables

A matrix-style table displaying the frequency distribution of variables, used to analyze relationships between categorical data.
- **Dichotomous Classification:** Data divided into only two mutually exclusive categories (e.g., Yes/No, Success/Failure).
- **Manifold Classification:** Data divided into more than two categories based on one or more characteristics.

### 6.2 Chi-Square Test of Independence

Used to determine if there is a significant association between two categorical variables. (Independence test and practical examples).
- **Test for 2x2 contingency tables** (Exact test for 2x2 tables).
- **Test for rc tables** (Test for rc tables).
- **Three-Way contingency tables:** Analysis involving three categorical variables simultaneously.
- **Example (CSE/Practical):** Testing if a person's living arrangement (Dormitory, On-Campus, etc.) is independent of their exercise frequency.
- **Yates's Correction:** An adjustment applied to $2 \times 2$ contingency tables when expected cell frequencies are small (typically less than 5) to prevent overestimation of statistical significance.

### 6.3 Additional Tests for Categorical Data

- **Large Sample Test of Significance:** Hypothesis tests based on the normal approximation, valid for large sample sizes (e.g., Z-test for proportions).
- **Bartlett’s test for homogeneity of variances:** A test used to check if two or more groups have equal variances.
- **Test for correlation and Regression coefficients:** Hypothesis tests to determine if a sample correlation coefficient or regression slope is significantly different from zero.

---

## Chapter 7
## Non-Parametric Tests

Non-parametric tests are "distribution-free" because they do not assume the data follows a specific distribution (like the normal distribution). (Non-parametric Test).

**Advantages:**
- Useful for small samples or non-normal data.
- Can handle nominal (categorical) or ordinal (ranked) data.
- Robust against outliers.

### 7.1 Specific Tests

- **Sign Test (One Sample and two Sample Sign Test):** Tests hypotheses about the population median based on the direction (+ or -) of differences rather than numerical magnitude.
    - **One Sample Sign Test:** Tests if the population median equals a specific value.
    - **Two Sample Sign Test (Paired):** Tests if two dependent samples differ in their medians.
- **Run Test (Run Test):** Used to assess the randomness of a sequence of observations.
- **Median Test:** A procedure to test if two independent samples differ in their central tendencies.
- **Mann-Whitney U Test (Rank Sum Test):** A popular alternative to the independent t-test for comparing two groups when normality assumptions are violated.

---

## Quick Reference Summary

| Chapter | Core Topic | Key Terms |
| --- | --- | --- |
| 1 | Foundational Concepts | Population, Sample, Parameter ($\mu$, $\sigma^2$), Statistic ($\bar{x}$, $s^2$) |
| 2 | Theory of Estimation | Estimator, Estimate, Unbiasedness ($E[\bar{x}]=\mu$), Consistency, Efficiency, MLE |
| 3 | Sampling Distributions | $\chi^2$, t, F Distributions, Fisher's Lemma, Distribution of Median/Range/Correlation |
| 4 | Hypothesis Testing | $H_0$, $H_a$, $\alpha$, p-value, Type I/II Error, Power ($1-\beta$) |
| 5 | Decision Rules | Critical Region, Best Critical Region, Most Powerful Test, Standard Error |
| 6 | Categorical Data | Contingency Tables, $\chi^2$ Independence Test, Yates' Correction, rc Tables, Bartlett's Test |
| 7 | Non-Parametric Tests | Distribution-free, Sign Test (1 & 2 sample), Run Test, Mann-Whitney U Test |

---
*STAT-2111 — Theory of Statistics | Dept. of CSE, University of Rajshahi*





