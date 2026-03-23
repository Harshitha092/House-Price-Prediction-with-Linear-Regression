# 📊 Predictive Analysis Using Machine Learning

## House Price Prediction with Linear Regression

---

## 📌 Project Overview

This project focuses on building a **machine learning regression model** to predict house prices based on property characteristics and amenities.
It demonstrates the **end-to-end predictive analytics workflow**, including data understanding, preprocessing, feature selection, model training, evaluation, and interpretation.

The project was developed with the objective of applying machine learning techniques to predict outcomes using a real-world dataset.

---

## 🎯 Problem Statement

Given historical housing data, the goal is to **predict the selling price of a house** based on features such as area, number of bedrooms, bathrooms, parking availability, and various amenities.

Since the target variable (`price`) is continuous, this problem is treated as a **regression task**.

---

## 🗂 Dataset Description

* **Dataset Name:** Housing Price Dataset
* **Source:** Kaggle – *Housing Prices Dataset*
* **Records:** 545 residential properties
* **Target Variable:** `price`

Features Include:
* Structural attributes: area, bedrooms, bathrooms, stories, parking
* Amenities: main road access, guest room, basement, hot water heating, air conditioning
* Location preference: preferred area
* Furnishing status: furnished, semi-furnished, unfurnished

The dataset contains **no missing values or duplicates**, making it suitable for regression analysis without extensive cleaning.

Note: The dataset is included in this repository for learning and reproducibility purposes.

---

## 🛠 Tools & Libraries Used

* **Python**
* **Pandas, NumPy**
* **Scikit-learn**
* **Matplotlib**

---

## ⚙️ Methodology

The project follows a structured machine learning workflow:

### 1️⃣ Data Understanding & Profiling

* Examined dataset shape, column names, and data types
* Verified absence of missing values and duplicate records
* Analyzed basic statistical distributions to understand feature ranges

This step ensured familiarity with the dataset before modeling.

---

### 2️⃣ Data Cleaning & Preprocessing

* No columns were dropped, as all features were relevant to house pricing
* Categorical variables were identified and converted into numerical form
* Binary categorical features were encoded using **One-Hot Encoding**
* `drop_first=True` was applied to avoid multicollinearity

After preprocessing, the dataset consisted entirely of numerical features suitable for regression modeling.

---

### 3️⃣ Feature Selection & Target Definition

* **Target (y):** `price`
* **Features (X):** All remaining property and amenity attributes

This separation ensured there was **no data leakage** during model training.

---

### 4️⃣ Train–Test Split

* The data was split into **80% training** and **20% testing** sets
* `random_state=42` was used to ensure reproducibility

The training set was used for model learning, while the test set was reserved strictly for evaluation.

---

### 5️⃣ Feature Scaling

* Applied **StandardScaler** to normalize feature values
* Scaling was performed **after** train–test split
* The scaler was fitted only on training data to prevent data leakage

This step ensured all features contributed equally to the model.

---

### 6️⃣ Model Training

* A **Linear Regression** model was selected due to the continuous nature of the target variable
* The model was trained using the scaled training dataset

Linear regression was chosen for its simplicity, interpretability, and suitability as a baseline model.

---

### 7️⃣ Model Evaluation

The model was evaluated on unseen test data using standard regression metrics:

* **Mean Absolute Error (MAE)**
* **Root Mean Squared Error (RMSE)**
* **R² Score**

These metrics assess prediction accuracy and the model’s ability to explain price variation.

---

## 📈 Model Performance

* **Mean Absolute Error (MAE):** ~970,043
* **Root Mean Squared Error (RMSE):** ~1,324,507
* **R² Score:** ~0.65

An R² score of approximately **0.65** indicates that the model explains about **65% of the variation in house prices**, demonstrating a meaningful relationship between selected features and the target variable.

---

## 📊 Visualizations

The following visualizations were included to support model evaluation and interpretation:

* **Actual vs Predicted Prices:** Validates overall model performance
* **Residuals vs Predicted Values:** Checks error distribution and bias
* **Feature Coefficients Bar Plot:** Highlights the relative influence of features on house prices

These plots help bridge the gap between model metrics and business understanding.

---

## 🏁 Conclusion

This project successfully demonstrates a complete machine learning regression pipeline for predicting house prices.
The Linear Regression model achieved reasonable predictive performance and showed that property features and amenities have a meaningful impact on pricing.

While linear regression captured a substantial portion of the price variation, future improvements could include adding more location-specific or market-driven features, applying feature transformations, or exploring non-linear models.

---

## 👩‍💻 Author  
**Harshitha Salian**  
Analytics Professional | SQL · Power BI · Excel · Python  
📍 Dubai, UAE | [LinkedIn](https://www.linkedin.com/in/salianharshitha/) | [GitHub](https://github.com/Harshitha092)

