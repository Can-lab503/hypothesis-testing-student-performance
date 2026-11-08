# 多元假设检验：特征扩展
**[English](./03_multivariate_analysis.md) | 中文**

*(改编自论文第 4 章)*

## 1. Rationale for Multivariate Analysis
In educational assessment, variables such as final scores, attendance, and study hours are highly correlated. Testing them independently (univariate) can inflate the Type I error rate and miss the joint effect. Therefore, the dependent variable was expanded into a **3D vector** (Score, Attendance, Hours Studied), and the analysis was extended to Multivariate Analysis of Variance (MANOVA).

## 2. Statistical Methods and Prerequisites
- **Box's M Test**: Checked the homogeneity of covariance matrices across groups.
  *Result:* M = 28.332, p = 0.555. The assumption of covariance homogeneity was met.
- **Hotelling's T² Test**: Compared mean vectors between two groups (Extracurricular: Yes vs. No).
- **Wilks' Λ Test**: Compared mean vectors across multiple groups (Parental Involvement: Low, Medium, High).

## 3. Key Findings and Multivariate Insights

### Hotelling's T² Test (Extracurricular Activities)
- **Result**: F(3, 6599) = 1.210, p = 0.304.
- **Insight**: The multivariate main effect was **NOT significant**. 
- **Compare with Chapter 3**: The univariate t-test showed a significant difference (p = 0.016). However, once we jointly considered attendance and study hours, the tiny difference in exam scores was absorbed by the background noise of the multidimensional space.

### Wilks' Λ Test (Parental Involvement)
- **Result**: F(6, 13198) = 0.413, p = 0.871.
- **Insight**: No significant main effect. 
- **Interaction Effect**: Interestingly, the interaction term (Extracurricular × Parental Involvement) showed an edge-significant trend (p = 0.054). This suggests a potential synergistic mechanism that current statistical power couldn't fully confirm.

## 4. Conclusion: The Power of Joint Inference
The contrast between Chapter 3 and Chapter 4 revealed a profound statistical principle: **Single-indicator significance can be deceptive.** 

When dealing with high-dimensional data, evaluating variables in isolation often leads to false positives (conceptually similar to overfitting in Machine Learning). By moving from marginal distributions to joint distributions (MANOVA), we successfully mitigated the risk of inflated false positives caused by dimensional stacking. This multivariate perspective—learning from the interaction of multiple features rather than isolated columns—is exactly why I am eager to pursue further studies in Machine Learning and Artificial Intelligence.
