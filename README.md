# 💰 Loan Approval Prediction — Logistic Regression & Decision Tree

![Loan Prediction Banner](https://cdn.pixabay.com/photo/2018/01/18/07/44/money-3088307_1280.jpg)

## 📋 Project Agenda

1. [Overview](#overview)
2. [Dataset](#dataset)
3. [Data Understanding](#data-understanding)
4. [Data Preprocessing](#data-preprocessing)
5. [Model Training](#model-training)
6. [Hyperparameter Tuning](#hyperparameter-tuning)
7. [Model Evaluation](#model-evaluation)
8. [Results Summary](#results-summary)
9. [Conclusion](#conclusion)
10. [How to Run](#how-to-run)

---

## 🧩 Overview
This project focuses on predicting **loan approval outcomes** using machine learning.  
The goal is to classify whether a loan should be **approved** or **rejected** based on applicant information such as income, loan amount, credit history, and other demographic and financial factors.

Two key models are explored:
- **Logistic Regression** — for interpretable, linear decision boundaries.  
- **Decision Tree Classifier** — for rule-based, non-linear decision making.

---

## 💼 Dataset
The dataset contains information about loan applicants and their application results.  
Typical features include:

- **Applicant Income**  
- **Coapplicant Income**  
- **Loan Amount**  
- **Loan Term**  
- **Credit History**  
- **Gender, Marital Status, Education, Employment Type**  
- **Loan Status** *(Target Variable)*

---

## 👁️ Data Understanding
The data was first explored to identify missing values, outliers, and data distribution.  
A quick intuition phase helped identify relationships between **income, credit history, and approval likelihood** — setting the stage for meaningful feature preparation and model selection.

---

## ⚙️ Data Preprocessing
Key steps taken to prepare the data:
- Handled missing values appropriately.  
- Encoded categorical columns using **LabelEncoder**.  
- Standardized numerical features using **StandardScaler** for fair comparison between models.  

*(These steps ensured all features contributed proportionally to model training.)*

---

## 🤖 Model Training
Two models were built and compared:

- **Logistic Regression**  
  Tried with different penalties (`L1`, `L2`, `ElasticNet`) while keeping other hyperparameters fixed.

- **Decision Tree Classifier**  
  Tested multiple configurations manually and later optimized using GridSearchCV for the best combination of depth, leaf size, and splitting strategy.

---

## 🔍 Hyperparameter Tuning
Two tuning methods were applied:

1. **Manual Trials**  
   Predefined parameter combinations were tested for each model to get an initial understanding of performance patterns.

2. **GridSearchCV**  
   Exhaustive search over hyperparameter grids using cross-validation to find the best-performing model configuration automatically.

---

## 📈 Model Evaluation
Each model was evaluated using:
- **Accuracy Score**  
- **Confusion Matrix**  
- **Classification Report** (Precision, Recall, F1-Score)

Custom function `print_score()` provided a structured and readable summary of both training and testing results.

---

## 🏆 Results Summary
| Model | Best Params | Test Accuracy | Notes |
|--------|--------------|---------------|--------|
| Logistic Regression | Regularized with L2 | High | Stable generalization |
| Decision Tree | Optimized via GridSearchCV | Slightly lower | More interpretable rules |

The **Logistic Regression** model performed slightly better overall in generalization, while the **Decision Tree** gave better interpretability and pattern discovery.

---

## 🧩 Conclusion
The notebook demonstrates:
- The importance of **scaling** and **encoding** in preprocessing.  
- How **manual trials** help form intuition before grid search.  
- That **regularization and controlled depth** prevent overfitting effectively.  

Both models can serve different business contexts — Logistic Regression for quick risk scoring, and Decision Trees for explainable lending policies.

---

## ▶️ How to Run

1. Clone or download the notebook:
   ```bash
     git clone https://github.com/<your-username>/Loan_Approval_Model_Tuning.git
   cd Loan_Approval_Model_Tuning
   ```bash 
2. Install dependencies:
  ```bash
    pip install -r requirements.txt
  ```bash
3. Run the notebook:
  ```bash 
    jupyter notebook Model_Tuning_and_Evaluation_LogReg_Tree.ipynb
  ```bash
   
