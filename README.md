# Employee_promotion_prediction

## Employee Promotion Prediction using Machine Learning

📌 **Project Overview**

This project explores how machine learning can be used to understand and support employee promotion decisions.
Using historical employee data, I analyzed patterns related to promotion and built predictive models to identify key factors that influence promotion outcomes.

The goal of this project is not to replace HR decisions, but to provide a data-driven decision support tool that highlights high-potential employees.

This project was built as a learning-focused, end-to-end ML project covering data analysis, modeling, evaluation, and interpretation.


🎯 **Problem Statement**

Employee promotions often involve subjective judgment.
This project aims to answer:

What factors are most associated with employee promotion?

Can machine learning help recommend promotion eligibility?

Are promotion patterns consistent across different ML models?

Target Variable:
Promoted_or_Not

1 → Promoted

0 → Not Promoted


📂 **Dataset Description**

The dataset contains employee-level information including:

- Demographics: Gender, Marital Status, State of Origin

- Education & Recruitment: Qualification, Channel of Recruitment

- Performance & Training: Performance score, targets met, training attendance, training evaluation score

- Work History: Division, tenure, previous employers, disciplinary action


🔧 **Data Preparation & Feature Engineering**

Steps taken:

Inspected data types and cleaned inconsistencies

Handled missing values (e.g., grouping missing qualifications as Unknown)

Removed non-predictive identifiers (Employee ID)

Created new features:

Age (from Year of Birth)

Tenure (from Year of Recruitment)

Encoded categorical variables

Scaled numeric features for model stability


🔍 **Exploratory Data Analysis (EDA)**

Key observations from EDA:

The dataset is imbalanced (~8% promoted)

Promotion rates vary significantly by:

Qualification

Division

Promoted employees generally have:

Higher performance scores

Higher training evaluation scores

Demographic features (e.g., gender) showed minimal differences in promotion rates


🤖 **Model Development**
Models Used

- Logistic Regression : Chosen for interpretability and explainability

- Decision Tree : Used to validate patterns and capture non-linear relationships

- Handling Class Imbalance

Used class_weight='balanced'

Focused evaluation on Recall for promoted employees

Threshold Optimization

Adjusted probability threshold from 0.5 to 0.3

Reduced false negatives (missed promotion candidates)


📈 **Model Evaluation**

Evaluation metrics used:

- Confusion Matrix

- Classification Report

- Recall for promoted class (business priority)

The adjusted threshold improved the model’s ability to identify promotion-worthy employees while maintaining reasonable precision.


✅ **Validation: Cross-Model Agreement**

To increase confidence in the findings, I compared results from two different model types:

Logistic Regression (linear, coefficient-based) AND Decision Tree (rule-based, non-linear)

*Validation Outcome*

Despite their different learning approaches, both models consistently identified:

- Performance score

- Target achievement

- Training score average as the strongest drivers of promotion.

This agreement across models suggests that the observed promotion patterns are robust and not specific to a single algorithm.


💡 **Key Insights**

Performance-related features are the strongest predictors of promotion

Training quality matters more than training quantity

Past disciplinary actions negatively impact promotion likelihood

Demographic attributes showed limited influence, supporting fairness


🛠️ **Tools & Technologies**

- Python

- Pandas, NumPy

- Scikit-learn

- Matplotlib, Seaborn


🚀 **Conclusion**

This project demonstrates how machine learning can be applied responsibly to HR analytics by:

Providing explainable insights

Supporting fair decision-making

Validating findings across multiple models
