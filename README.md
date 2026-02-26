**Loan Approval Prediction using KNN**
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
📖 Project Overview

This project implements a K-Nearest Neighbors (KNN) classifier to predict whether a loan application will be approved based on applicant details.

The goal was to understand model training, evaluation, and real-world challenges like overfitting.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Dataset Description:**

The dataset contains applicant features such as:
- Gender
- Marital Status
- Education
- Applicant Income
- Loan Amount
- Credit History
- Loan Status (Target Variable)
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

⚙️ Steps Performed

- Data Checks and basic cleaning
- Train-Test split
- Handling missing values
- Handling Outliers
- Preprocessing using ColumnTransformer:
  - OneHotEncoding for categorical features
  - StandardScaler for numerical features
- Baseline KNN model training
- Cross Validation (5-Fold)
- Hyperparameter tuning using GridSearchCV
- Final model evaluation

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

📊**Model Performance before cross validation & HyperParameter Tuning **

- Training Accuracy: 75%
- Testing Accuracy: 57%

What Happened? — Understanding Overfitting

The model achieved higher accuracy on training data but significantly lower accuracy on testing data.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**What is Overfitting?**

Overfitting occurs when a model:
- Learns the training data too well
- Captures noise and patterns specific to training data
- Fails to generalize to unseen data
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
**Why Overfitting Happens in KNN?**

- Small K value can make the model too sensitive
- High feature dimensionality
- Noisy or imbalanced dataset
- Insufficient data

**Techniques to Overcome Overfitting**

_ Use Cross Validation
- Tune hyperparameter (Optimal K selection)
- Use proper feature scaling
- Reduce irrelevant features
- Try alternative models (Logistic Regression, Random Forest)

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
**Key Learning**

- This project highlights an important lesson:
-  High training accuracy does not guarantee good model performance.
- Model evaluation must focus on generalization ability.
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

🚀** Model Improvement Using Cross Validation & Hyperparameter Tuning**
- To address overfitting, the following steps were applied:
- 5-Fold Cross Validation for reliable performance estimation
- Hyperparameter tuning using GridSearchCV
- Optimal selection of K (n_neighbors)

- Important:
- Cross Validation improves reliability — not necessarily accuracy.
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

📊 Improved Model Performance

- Training Accuracy: 69%
- Testing Accuracy: 66%
- Cross Validation Mean Accuracy: 66%
- This reduced the performance gap and improved model stability.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Tech Stack
- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib / Seaborn

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

💡 Final Note
📈 Before vs After Improvement

| Stage             | Training Accuracy | Testing Accuracy |
| ----------------- | ----------------- | ---------------- |
| Initial Model     | 75%               | 57%              |
| After CV & Tuning | 69%               | 66%              |

In real-world Machine Learning projects, models may not always perform perfectly.
Building a model is easy.
Building a reliable model requires validation and tuning.
Understanding why a model underperforms or overperforms is as important as building it.
