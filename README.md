# 🎓 Student Performance and Stress Predictive Modeling

## Project Overview

This project implements a comprehensive Machine Learning pipeline to predict two distinct, yet related, outcomes for students: their **Academic Performance (GPA)** and their **Perceived Stress Level**. The analysis explores the complex interrelationship between personal data, study habits, and environmental factors on student success and well-being.

The primary goal was not just to achieve high accuracy, but to conduct a **critical comparative analysis** between simple, interpretable models (Linear Regression, Logistic Regression, LDA) and complex ensemble methods (Random Forest, XGBoost). This approach demonstrates a commitment to **model efficiency and parsimony**, a key requirement in real-world ML engineering.

## 🎯 Key Predictive Tasks

| Task | Objective | Methodologies Explored | Core Metrics |
| :--- | :--- | :--- | :--- |
| **Academic Performance** | Predict the final Grade Point Average (GPA), modeling it as a **Regression** problem. | Linear Regression, Random Forest, XGBoost | $R^2$ Coefficient of Determination, MAE (Mean Absolute Error) |
| **Stress Level** | Classify students into Low, Moderate, or High stress categories (**Multi-class Classification**). | Logistic Regression, LDA, KNN, Random Forest, XGBoost | Accuracy, F1-Score, Confusion Matrix |

## 💡 Analytical Highlights and Conclusions

### 1. Model Efficiency Over Complexity

For the classification task (predicting stress and academic success binary outcomes), models based on linear methods, specifically **Logistic Regression and Linear Discriminant Analysis (LDA)**, proved to be the most effective.

* These simple models matched or exceeded the performance of highly complex methods like **Random Forest and XGBoost**, even after extensive hyperparameter optimization on the latter.
* **Conclusion:** This highlights a critical finding: the simplicity of the underlying data relationship meant the extra complexity and computational cost of ensemble models were unnecessary, demonstrating a strong principle of **parsimonious model selection**.

### 2. Isolation of the Single Strongest Factor (Univariate Modeling)

By selectively isolating variables, a **Univariate Linear Regression Model** was constructed to predict GPA based solely on the variable **'Hours Studied Per Day.'**

* **Result:** The model achieved a **Coefficient of Determination ($R^2$) of 0.55**.
* **Significance:** In a complex, multi-factorial domain like human behavior/education, an $R^2$ of 0.55 using only one predictor is remarkably high. This identified 'Hours Studied Per Day' as the most impactful and actionable variable, confirming a direct and measurable relationship:
$$
\text{Predicted GPA} \approx \beta_0 + \beta_1 \cdot (\text{Study Hours})
$$

### 3. Critical Assessment of Data Leakage

Initial models (e.g., XGBoost) showed nearly perfect accuracy in predicting the *original* stress score. This was critically evaluated and attributed to the variable's deterministic calculation from other features in the dataset (a form of data leakage or circularity). This finding reinforces the commitment to **data integrity** and the difference between high model scores and true predictive power.

## 🛠️ Technical Stack

* **Language:** Python 3
* **Core Libraries:** `pandas`, `numpy`, `scikit-learn` (for core ML), `xgboost` (for gradient boosting comparison), `matplotlib`, `seaborn` (for visualization).
* **Skills Demonstrated:** Comparative model assessment, regression and multi-class classification, hyperparameter tuning, data visualization, and critical analysis of model performance metrics.

## 📁 Repository Contents

* `Predicción_de_promedio_academico_y_nivel_de_estrés_en_estudiantes.ipynb`: The complete analysis notebook containing all data preprocessing, visualization, model training, and comparative evaluation steps.

---
**Authors:** Baltazar Salvatierra and Victoria Di Paolo

