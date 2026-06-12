# Corporate Bankruptcy Prediction: A Multivariate Analysis

## Overview
This project applies multivariate statistical techniques to predict corporate bankruptcy using a benchmark dataset of financial ratios representing solvency, profitability, and liquidity. The objective is to effectively distinguish between financially sound and bankrupt firms through a rigorous pipeline of data preprocessing, dimensionality reduction, probabilistic classification, and unsupervised clustering.

## Methodology
* **Data Preprocessing:** Addressed severe skewness and heteroscedasticity in the raw data by applying Box-Cox transformations and Mahalanobis distance-based outlier excision.
* **Dimensionality Reduction:** Utilized Principal Component Analysis (PCA) to compress the feature space, successfully isolating the primary discriminative signal into a single dominant vector while discarding orthogonal noise.
* **Probabilistic Classification:** Built and evaluated generative (LDA, QDA, Naive Bayes) and discriminative (Logistic Regression) models, rigorously validating performance via a 2000-iteration Monte Carlo Cross-Validation framework.
* **Unsupervised Clustering:** Explored the natural geometric structure of the data using standard k-means, mean-seeded k-means, and a hybrid LDA-projected k-means approach.

## Key Findings
* **The Power of Preprocessing:** While raw financial data required complex non-linear models like QDA due to variance violations, effective data transformation allowed simpler linear models (LDA and Logistic Regression) to achieve highly optimal decision boundaries.
* **Optimal Classifier:** Linear Discriminant Analysis (LDA) on transformed data emerged as the superior predictive model, maintaining a robust harmonic balance between Precision and Recall.
* **Clustering Success:** The hybrid LDA + k-means clustering strategy achieved an impressive unsupervised accuracy of **82.80%**. By maximizing between-group variance before clustering, the model was mathematically guaranteed to find an optimal classification boundary.
* **Conclusion:** Rigorous structural transformations and PCA fundamentally simplify noisy financial data, allowing both parsimonious linear classifiers and optimized clustering algorithms to achieve robust class discrimination.
