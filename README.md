# Medical Insurance Cost Classification — Summative Assignment

**Author:** Armand Kayiranga  
**Email:** a.kayiranga1@alustudent.com  
**Course:** Introduction to Machine Learning (BSE)  
**Institution:** African Leadership University  

---

## 📌 Problem Statement

The goal of this project is to predict whether a person will incur high or low medical insurance costs based on personal attributes such as age, sex, BMI, number of children, smoking status, and region. This is framed as a binary classification task.

---

## 🗂️ Dataset Used

The dataset used is a public medical insurance dataset (sourced from external open data repositories), where the target variable was engineered as a binary label (`high_cost`) by comparing charges to the dataset median. The dataset includes both numerical and categorical features.

---

## 🧠 Models Implemented

### Classical Machine Learning Models:
- Logistic Regression
- Support Vector Machine (SVM)

### Neural Network Models:
- One unoptimized baseline neural network
- Three optimized models using various techniques:
  - Optimizers (Adam, RMSprop)
  - Regularization (L1, L2)
  - Dropout
  - Early Stopping
  - Learning Rate adjustments
  - Number of Layers

---

## 📊 Optimization Results Table (Neural Network)

| Instance | Optimizer | Regularizer | Epochs | Early Stopping | Layers | LR     | Accuracy | Precision | Recall | F1-score |
|----------|-----------|-------------|--------|----------------|--------|--------|----------|-----------|--------|----------|
| 1        | Default   | None        | 50     | No             | 2      | 0.001  | 0.78     | 0.75      | 0.76   | 0.75     |
| 2        | Adam      | None        | 50     | No             | 2      | 0.001  | 0.80     | 0.77      | 0.79   | 0.78     |
| 3        | RMSprop   | L2          | 50     | Yes            | 2      | 0.001  | 0.82     | 0.81      | 0.80   | 0.80     |
| 4        | Adam      | L1 + Dropout| 100    | Yes            | 3      | 0.0005 | 0.85     | 0.84      | 0.83   | 0.83     |

---

## ✅ Summary of Findings

- The best-performing model was **Instance 4**, a neural network using:
  - Adam optimizer
  - L1 regularization
  - Dropout
  - Early stopping
  - A low learning rate of 0.0005
  - 3 layers

- **Classical ML vs Neural Network**:
  - While SVM and Logistic Regression achieved competitive results (~80%), the optimized neural network (Instance 4) achieved higher performance in all metrics, especially in generalizing on unseen data.

---

## 🗂️ Project Structure
