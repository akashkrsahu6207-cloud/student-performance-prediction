🎓 Student Performance Prediction Using Machine Learning


📌 Project Overview

This project aims to predict a student’s final exam grade (G3) using various academic, demographic, and social factors. The objective is to analyze which features influence student performance and build a machine learning model capable of accurately predicting final grades.

This is a regression-based machine learning project, where the target variable is continuous (final marks).





🎯 Problem Statement

Educational institutions often want to identify students who may need academic support before final examinations. By predicting final grades using earlier performance indicators and related attributes, we can:

Identify at-risk students

Understand key performance drivers

Support data-driven decision making

Improve overall academic outcomes

The goal of this project is to build and compare regression models to predict the final grade (G3).






📊 Dataset Information

The dataset contains information about 395 students along with their academic and personal attributes.

🔹 Important Features:

age – Age of student

sex – Gender

studytime – Weekly study time

failures – Number of past class failures

absences – Number of school absences

G1 – First period grade

G2 – Second period grade

G3 – Final grade (Target Variable)

🎯 Target Variable:

G3 – Final exam grade






🛠️ Technologies Used

Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn






🔍 Project Workflow
1️⃣ Data Loading

The dataset was loaded using Pandas and initial inspection was performed using:

.head()

.info()

.describe()

2️⃣ Data Cleaning & Preprocessing

The following preprocessing steps were applied:

Checked for duplicate values

Checked for missing values

Converted categorical variables into numerical form using:

Label mapping

pd.get_dummies()

Performed Train-Test Split (80% training, 20% testing)

3️⃣ Exploratory Data Analysis (EDA)

EDA was performed to understand the relationship between features and the target variable.

🔹 Correlation Analysis

A heatmap was used to visualize correlations between features.

Key Observation:

G1 and G2 show strong positive correlation with G3.

Study time and failures also influence final performance.

🔹 Scatter Plot Analysis

A scatter plot between G2 and G3 showed a strong linear relationship.

Observation:
Students who perform well in the second period generally score high in final exams.

🤖 Model Building

The dataset was divided into training and testing sets.

Two regression models were implemented:

1️⃣ Linear Regression

Used as a baseline model

Captures linear relationships between variables

2️⃣ Random Forest Regressor

Ensemble learning method

Handles non-linear relationships effectively

Provides improved predictive performance

📈 Model Evaluation
📊 Evaluation Metric Used:

R² Score (Coefficient of Determination)

R² Score measures how well the model explains variance in the target variable.

R² = 1 → Perfect prediction

R² = 0 → No explanatory power

R² < 0 → Poor model performance

📊 Model Performance Comparison
Model	R² Score

Random Forest	(0.860)

Conclusion:
Random Forest performed better than Linear Regression as it captured complex relationships between features more effectively.




🔥 Feature Importance (Random Forest)

Feature importance was extracted from the trained Random Forest model.

Top Contributing Features:

G2 (Second Period Grade)

G1 (First Period Grade)

Study Time

Failures

Absences

This indicates that previous academic performance is the strongest predictor of final grades.






🧠 Key Insights

Previous grades strongly impact final grade prediction.

Students with more failures tend to score lower.

Higher study time generally improves academic performance.

Absenteeism negatively affects final results.






🚀 Future Improvements

Perform hyperparameter tuning using GridSearchCV

Apply Cross-Validation for better model evaluation

Experiment with advanced models such as XGBoost

Deploy the model using Streamlit

Build a user-friendly prediction web application






📁 Project Structure
student-performance-prediction/
│
├── data/
│   └── student_data.csv
│
├── notebook/
│   └── student_performance.ipynb
│
├── README.md
└── requirements.txt






🏁 Conclusion

This project demonstrates how machine learning techniques can be applied to educational data to predict student performance. By analyzing academic and personal attributes, we successfully built regression models capable of predicting final grades.

Random Forest provided better predictive performance compared to Linear Regression due to its ability to model complex relationships.






This project showcases:

Data preprocessing

Exploratory data analysis

Regression modeling

Model comparison

Feature importance analysis
