# Univariate Hypothesis Testing in Educational Assessment
**[中文版](./02_univariate_hypothesis_testing.zh.md) | English**

*(Adapted from Chapter 3 of the thesis)*

**Dataset:** [Student Performance Factors (Kaggle)](https://www.kaggle.com/datasets/lainguyn123/student-performance-factors) 
**Sample Size:** N = 6,607

## 1. Exploratory Data Analysis and Assumption Verification
Before conducting parametric tests, rigorous assumption checks were performed:
- **Normality**: Visualized via histograms with normal curves and Q-Q plots (see `figures/`). While Kolmogorov-Smirnov tests rejected strict normality for some subgroups, the large sample size (N = 6,607) ensures that the Central Limit Theorem (CLT) holds, making the t-test robust.
- **Variance Homogeneity**: Levene's test revealed slight variance heterogeneity (p = 0.028) between extracurricular groups. However, given the large sample size and the nearly identical standard deviations (ratio ≈ 1.03), standard t-test results were deemed reliable.
- **Outliers**: Outliers in `Hours_Studied` and `Final_Exam_Score` were retained after confirming they represented genuine behavioral variations rather than data entry errors.

## 2. Test Selection and Empirical Results
Three univariate tests were conducted to investigate different factors. 

### Case A: Chi-square (χ²) Test of Independence (Internet Access vs. Pass Rate)
- **Result**: χ² = 1.054, df = 1, p = 0.305.
- **Interpretation**: No significant association. Having internet access does not independently determine exam passing, likely due to the diminishing "threshold effect" of internet access in modern education.

### Case B: Independent Samples t-test (Extracurricular Activities vs. Score)
- **Result**: t = 2.402, df = 6605, p = 0.016.
- **Interpretation**: Statistically significant. Students participating in extracurriculars scored slightly higher (Mean Diff = 0.5277).

### Case C: One-way Analysis of Variance (ANOVA) (Parental Involvement vs. Score)
- **Result**: F(2, 6604) = 0.420, p = 0.657.
- **Interpretation**: No significant overall difference across Low, Medium, and High involvement groups.

## 3. Critical Reflection: The Distinction Between Statistical and Practical Significance
The most valuable lesson from this chapter emerged from **Case B**. 
While the p-value (0.016) crossed the significance threshold, the actual difference in mean scores was merely **0.5277 points** on a 100-point scale, with the distributions almost entirely overlapping (see `figures/03_score_by_extracurricular_boxplot.png`).

**Key Takeaway for AI/DS:** 
At a massive sample size (N = 6,607), the p-value easily detects tiny, practically meaningless differences. In Data Science, blindly trusting statistical significance without checking effect sizes is dangerous. This experience taught me to evaluate metrics contextually—a mindset directly applicable to evaluating machine learning models, where a statistically significant feature might have zero practical predictive power.
