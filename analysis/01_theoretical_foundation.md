# Theoretical Foundation: Connections & Multivariate Extensions
**[中文版](./01_theoretical_foundation.zh.md) | English**

*(Adapted from Chapter 2 of the thesis)*

## 1. Interconnections Among the Three Distributions
The χ², t, and F distributions are **not independent distributions**; rather, they are closely interconnected and can be derived from one another, forming a coherent core of statistical inference.

- **χ² distribution**: Arises as the sum of squares of independent standard normal variables, serving as the foundation for variance-related inference.
- **t distribution**: Constructed from the ratio of a standard normal variable to the square root of an independent χ² variable divided by its degrees of freedom, used for inference about means when the sample size is small and the variance is unknown.
- **F distribution**: Defined as the ratio of two independent χ² variables, each divided by its respective degrees of freedom, used for comparing variances and in analysis of variance (ANOVA).

**Key Mathematical Relationships:**
- The construction of the t-distribution inherently relies on the χ² distribution.
- Squaring a t-variable yields an F-distribution: t² ~ F(1, n). This bridges inference about means and inference about variances.
- As the denominator degrees of freedom n₂ approaches infinity (n₂ → ∞), n₁F converges in distribution to χ²(n₁), revealing the asymptotic consistency between the F-test and the χ²-test.

## 2. Extension to the Multivariate Context
When moving from univariate to multivariate analysis, these distributions generalize to handle joint inference problems across multiple indicators. This transition is essential for modern AI and Data Science, where models must learn from high-dimensional feature spaces.

| Univariate Distribution | Multivariate Generalization | Primary Use Case |
| :--- | :--- | :--- |
| χ² distribution | **Box's M Test** | Tests the homogeneity of covariance matrices across multiple populations. |
| t distribution | **Hotelling's T² Test** | Tests the equality of mean vectors between two multivariate populations. |
| F distribution | **Wilks' Λ Test** | Tests the equality of mean vectors across multiple groups (MANOVA). |

**Theoretical Continuity:**
Hotelling's T² Test can be transformed into an F-distribution; Wilks' Λ Test can be approximated by an F or χ² distribution under large samples; and Box's M Test statistic asymptotically follows a χ² distribution. Mastering the univariate properties is the foundation for understanding these advanced multivariate methods used in Chapters 3 and 4.
