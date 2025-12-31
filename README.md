# 🎓 Student Performance Analysis & Grade Prediction

This project investigates the social, demographic, and academic factors that influence student success in secondary education. Using the **UCI Student Performance Dataset**, I performed an end-to-end analysis—from deep data exploration and feature engineering to building predictive models for final grades.

## 📌 Project Objectives

* **Identify Key Influencers:** Determine which factors (e.g., parental education, study time, alcohol consumption) most strongly correlate with academic success.
* **Predict Success (Classification):** Build a model to predict whether a student will pass (G3  10) or fail.
* **Predict Exact Grades (Regression):** Use multiple linear regression to predict a student's specific final score (0–20).

## 📊 Dataset Overview

The data encompasses student achievement in two subjects: **Mathematics** and **Portuguese**.

* **Features:** 30 attributes including school, sex, age, address, family size, parental job, study time, failures, and social activities.
* **Target Variables:** G1 (1st period), G2 (2nd period), and **G3 (Final Grade)**.

## 🛠️ Analysis Workflow

### 1. Exploratory Data Analysis (EDA)

* Analyzed the **Mathematics vs. Portuguese** distributions, noting that Portuguese grades generally have a higher mean and lower standard deviation.
* Used **Box Plots** and **Categorical Analysis** to evaluate features.
* *Insight:* Female students performed better in Portuguese, while male students performed better in Math.
* *Insight:* Higher parental education level (Medu/Fedu) correlates strongly with higher student grades.



### 2. Feature Engineering & Selection

* **Banding:** Grouped the `absences` feature into bands to reduce noise and reveal the clear downward trend in grades as absences increase.
* **Feature Removal:** Dropped statistically insignificant features (like `famsize` and `Pstatus`) to improve model efficiency.
* **Mapping:** Converted categorical text data into numerical formats (Label Encoding) for model compatibility.

### 3. Machine Learning Models

* **Logistic Regression:** Achieved ~**89% accuracy** in predicting Pass/Fail outcomes for Math and ~**92%** for Portuguese.
* **Multiple Linear Regression:** Predicted exact G3 scores.
* Initially impacted by "Zero-Grade" outliers (students who missed the final exam).
* After removing outliers, the model achieved an  of **0.92**, significantly reducing the Mean Squared Error (MSE).



## 🚀 Key Technologies

* **Python:** Core programming language.
* **Pandas & NumPy:** Data manipulation and cleaning.
* **Seaborn & Matplotlib:** Advanced data visualization.
* **Scikit-Learn:** Machine learning (Logistic Regression, Linear Regression, Train-Test Split).

## 📈 Conclusion

The analysis proves that while socio-economic factors matter, **previous academic performance (G1 & G2)** and **school attendance** are the strongest predictors of a student's final grade.

---