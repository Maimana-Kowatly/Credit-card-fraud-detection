# 🛡️ Credit Card Fraud Detection using Machine Learning

In today’s digital economy, credit card fraud is a pressing challenge that threatens both consumers and financial institutions. This project tackles fraud detection by developing robust machine learning models that emphasize **recall**, ensuring fraudulent transactions are caught even in the presence of extreme class imbalance.

---

## 📌 Objective

To build and evaluate machine learning models capable of accurately identifying fraudulent credit card transactions within a highly imbalanced dataset, with a strong focus on **maximizing recall**.

---

## 💼 Business Context

- Global credit card fraud losses are estimated in the **billions of dollars**.
- False **negatives** (missed frauds) can lead to significant financial and reputational damage.
- False **positives** (flagging valid transactions) can frustrate customers and disrupt trust.
- Hence, this project prioritizes **sensitivity (recall)** over simple accuracy.

---

## 📊 Dataset Overview

- **Source**: Kaggle - Credit Card Fraud Detection dataset
- **Transactions**: ~284,807 total
- **Fraudulent**: < 0.2% (~492 cases)
- **Features**:
  - `V1` to `V28`: PCA-transformed, anonymized features
  - `Time`: Seconds since first transaction
  - `Amount`: Transaction amount
  - `Class`: Target variable (1 = fraud, 0 = legitimate)

---

## 🧪 Methodology

### 1. 📈 Exploratory Data Analysis (EDA)
- Uncovered extreme class imbalance
- Visualized distributions and fraud patterns
- Guided choice of preprocessing and sampling strategies

### 2. ⚙️ Preprocessing
- **Stratified split** to maintain fraud ratio
- **Feature scaling** to normalize input distributions

### 3. ⚖️ Handling Class Imbalance
- Compared four strategies:
  - **Imbalanced**: Original skewed dataset
  - **Random Oversampling**
  - **SMOTE**
  - **ADASYN** (adaptive synthetic sampling)

### 4. 🤖 Model Development
- **Logistic Regression**: Baseline
- **Decision Tree**: Captures non-linearities
- **XGBoost**: High-performance, ensemble-based model

Each algorithm was trained under all four sampling methods.

---

## 🏆 Best Model

- **Model**: XGBoost
- **Sampling Strategy**: ADASYN
- **Metrics**:
  - **ROC AUC**: ~0.98
  - **Recall**: **0.86**
  - Balanced performance, especially on detecting fraudulent cases

📌 The combination of **XGBoost + ADASYN** achieved the best balance between recall and precision, proving effective in catching hard-to-detect fraud cases.

---

## 📁 Files

- `.ipynb`: Main Jupyter notebook containing code, analysis, and visualizations
- `README.md`: Project overview and documentation

---

## 🧠 Key Learnings

- Imbalanced data requires **specialized preprocessing** and **targeted sampling**.
- **Recall** is crucial in fraud detection, more than overall accuracy.
- XGBoost, combined with **adaptive sampling**, can effectively handle class imbalance and improve fraud detection rates.

---

## 📚 How to Run

1. Clone the repository
2. run the .ipynb files
