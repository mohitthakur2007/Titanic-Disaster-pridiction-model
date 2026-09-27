# Titanic Disaster Prediction Model

A machine learning project that analyzes passenger data from the Titanic disaster and builds classification models to predict passenger survival based on demographic and ticket features.

---

## Overview

This project explores the Titanic dataset to uncover demographic insights related to survival rates and trains two machine learning classifiers—**Logistic Regression** and **Decision Tree**—to predict whether a given passenger survived (1) or did not survive (0).

---

## Dataset & Features

The dataset undergoes initial cleaning by dropping non-predictive identifiers (`Name`, `PassengerId`, `Cabin`, `Ticket`, `Embarked`) and encoding categorical columns.

### Included Features

* `Pclass`: Passenger class (1 = 1st, 2 = 2nd, 3 = 3rd)
* `Sex`: Gender (Encoded: `1` for Male, `0` for Female)
* `Age`: Age of the passenger in years (Missing values imputed using dataset median)
* `SibSp`: Number of siblings/spouses aboard the Titanic
* `Parch`: Number of parents/children aboard the Titanic
* `Fare`: Passenger fare price
* `Survived`: **Target variable** (1 = Survived, 0 = Did not survive)

---

## Key Exploratory Data Analysis (EDA) Insights

* **Overall Survival Rate:** ~38.38%
* **Gender Disparity:**
  * **Female Survival Rate:** ~74%
  * **Male Survival Rate:** ~19%
* **Passenger Class Impact:**
  * **1st Class:** 63% survival rate
  * **2nd Class:** 47% survival rate
  * **3rd Class:** 24% survival rate
* **Age Distribution:** The majority of passengers belonged to the 20–30 age group.

---

## Machine Learning Models & Results

The dataset was split into an **80% training set** (712 rows) and a **20% testing set** (179 rows).

| Model | Accuracy | Precision (Survived=1) | Recall (Survived=1) | F1-Score (Survived=1) |
| :--- | :--- | :--- | :--- | :--- |
| **Logistic Regression** | **79.33%** | 0.78 | 0.69 | 0.73 |
| **Decision Tree** | **75.42%** | 0.70 | 0.70 | 0.70 |

### Key Takeaways
* **Logistic Regression** outperformed the Decision Tree model on this dataset.
* Linear decision boundaries (like Logistic Regression) tend to perform better on smaller datasets with simpler feature relationships (e.g., strong direct correlations between survival and gender/class/fare).

---

## Installation & Usage

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/titanic-survival-prediction.git](https://github.com/your-username/titanic-survival-prediction.git)
   cd titanic-survival-prediction
