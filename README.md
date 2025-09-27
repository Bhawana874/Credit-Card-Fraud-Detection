# Credit-Card-Fraud-Detection
# 💳 Credit Card Fraud Detection using XGBoost & SHAP

This project demonstrates how machine learning can be applied to detect fraudulent transactions in digital financial services. Using the well-known **Credit Card Fraud Detection dataset** (from Kaggle), I trained an **XGBoost classifier** and applied **SHAP** for explainability. This work supplements my prior research on anomaly detection and links directly to **data protection and AI governance** frameworks (GDPR, India’s DPDP, Kenya’s DPA).

---

## 📂 Dataset

* **Source:** [Kaggle – Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
* **Description:** 284,807 anonymized credit card transactions, with PCA-transformed features (`V1`–`V28`), `Time`, `Amount`, and target label `Class` (0 = normal, 1 = fraud).
* **Imbalance:** Only ~0.17% transactions are fraudulent → highly imbalanced classification task.

---

## 🧪 Methods

### 1. Preprocessing

* Train/test split (70/30) with stratification.
* Features standardized where necessary.
* Class imbalance considered during evaluation (AUC, Precision/Recall).

### 2. Models

* **XGBoost Classifier** (gradient boosting on decision trees).
* **Metrics Used:** Precision, Recall, F1-score, ROC-AUC.
* **Explainability:** SHAP (Shapley Additive Explanations) to identify top features driving fraud predictions.

---

## 📊 Results

* **Precision (Fraud):** 94%
* **Recall (Fraud):** 76%
* **F1 (Fraud):** 0.84
* **Overall AUC:** 0.9285

### Key Insights

* Features **V14, V4, V22** emerged as the most important in fraud classification.
* SHAP summary plots demonstrated how high/low feature values push transactions toward fraud vs. non-fraud classification.
* This aligns with regulatory requirements for **AI transparency** and explainability in financial systems.

---

## 🛠️ Tech Stack

* Python (Google Colab / Jupyter)
* [XGBoost](https://xgboost.readthedocs.io/)
* [scikit-learn](https://scikit-learn.org/)
* [SHAP](https://github.com/shap/shap)

---

## 🚀 How to Run

1. Clone this repository:

   ```bash
   git clone https://github.com/Bhawana874/credit-card-fraud-detection.git
   cd credit-card-fraud-detection
   ```
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Run in Jupyter/Colab:

   ```python
   python fraud_detection_xgboost.py
   ```

---

## 🔍 Research Relevance

This project goes beyond classification performance:

* Demonstrates **AI transparency** via SHAP in line with GDPR’s “right to explanation”.
* Highlights challenges of **class imbalance** in DFS fraud detection.
* Provides reproducible evidence linking **AI + financial data protection frameworks**.

---

## 📖 References

* [Kaggle: Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
* Lundberg, S. & Lee, S. (2017). A Unified Approach to Interpreting Model Predictions (SHAP).
* GDPR / DPDP / Kenya DPA legal provisions on transparency & fairness.

---

## ✨ Author

**Bhawana Sharma**
🔗 [GitHub Profile](https://github.com/Bhawana874)
👩‍💻 Researcher in AI and Cybersecurity
