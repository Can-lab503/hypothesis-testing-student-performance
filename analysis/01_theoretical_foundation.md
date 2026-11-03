# Theoretical Foundation: Connections & Multivariate Extensions

*(Adapted from Chapter 2 of the thesis)*

## 1. Intrinsic Connections of the Three Distributions
The chi-square (χ²), t, and F distributions are not isolated statistical tools; they form a rigorous hierarchical system derived from the standard normal distribution:
- **χ² distribution**: Originates from the sum of squares of independent standard normal variables (foundation for variance tests).
- **t distribution**: Constructed from the ratio of a standard normal variable to the square root of an independent χ² variable (used for mean inference with small samples).
- **F distribution**: The ratio of two independent χ² variables, each divided by their respective degrees of freedom (used for variance comparison and ANOVA).

**Key Mathematical Relationships:**
- The construction of the t-distribution inherently depends on the χ² distribution.
- Squaring a t-variable yields an F-distribution: t² ~ F(1, n). This bridges mean testing and variance analysis.
- As the denominator degrees of freedom n₂ approaches infinity (n₂ → ∞), n₁F converges in distribution to χ²(n₁), revealing the asymptotic consistency between the F-test and the χ²-test.

## 2. Extension to Multivariate Settings
When moving from univariate to multivariate analysis, these distributions generalize to solve joint inference problems across multiple indicators. This transition is crucial for modern AI and Data Science, where models must learn from high-dimensional feature spaces.

| Univariate Distribution | Multivariate Generalization | Primary Use Case |
| :--- | :--- | :--- |
| χ² distribution | **Box's M Test** | Tests the homogeneity of covariance matrices across multiple populations. |
| t distribution | **Hotelling's T²** | Tests the equality of mean vectors between two multivariate populations. |
| F distribution | **Wilks' Λ** | Tests the equality of mean vectors across multiple groups (MANOVA). |

**Theoretical Continuity:**
Hotelling's T² can be transformed into an F-distribution; Wilks' Λ can be approximated by an F or χ² distribution under large samples; and Box's M statistic asymptotically follows a χ² distribution. Mastering the univariate properties is the foundation for understanding these advanced multivariate methods used in Chapters 3 and 4.
