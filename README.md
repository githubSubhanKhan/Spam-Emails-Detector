# 📧 Spam Email Detector

A **Machine Learning–based Spam Email Detection system** that classifies emails as **Spam** or **Not Spam** using **Logistic Regression** and **TF-IDF text vectorization**.  
The model is trained on a Kaggle dataset and achieves **95% accuracy**, with special focus on minimizing **false positives**, which is critical in real-world email systems.

---

## 🚀 Project Overview

Email spam detection is a real-world problem where incorrectly marking a **legitimate email as spam** can cause serious issues.  
This project builds a reliable spam classifier that prioritizes **precision** and reduces the risk of false alarms.

---

## 📂 Dataset

- Dataset imported from **Kaggle** using `kagglehub`
- Total rows: **5572**
- Original features: **5**
- Useful features selected: **2**
- Unnecessary features were removed to improve model efficiency
- Label **"ham"** was replaced with **"not spam"** for better understanding

---

## 🛠️ Technologies & Libraries Used

- **Python**
- **kagglehub** – Dataset import
- **pandas, numpy** – Data manipulation
- **scikit-learn**
  - `train_test_split` – Dataset splitting
  - `LogisticRegression` – Classification model
  - `LabelEncoder` – Encoding categorical labels
  - `TfidfVectorizer` – Text feature extraction
  - `confusion_matrix`, `accuracy_score` – Model evaluation

---

## ⚙️ Methodology

1. Imported the dataset from Kaggle using `kagglehub`
2. Analyzed dataset structure using `.info()`
3. Dropped irrelevant features
4. Replaced `"ham"` with `"not spam"`
5. Converted email text into numerical features using **TF-IDF Vectorizer**
6. Encoded class labels using **LabelEncoder**
7. Split dataset:
   - **75% Training**
   - **25% Testing**
8. Trained a **Logistic Regression** classifier
9. Evaluated model using **accuracy score** and **confusion matrix**
10. Added custom email input for real-time prediction

---

## 📊 Model Performance

- **Accuracy:** `95%`

### Confusion Matrix


| Metric | Value |
|------|------|
| True Negatives (TN) | 1202 |
| True Positives (TP) | 129 |
| False Positives (FP) | 0 |
| False Negatives (FN) | 62 |

### 🔍 Key Insight

For email classification, **false positives matter the most** because:
> ❌ A legitimate email marked as spam can result in loss of important information.

This model achieves **zero false positives**, making it safer for real-world use.

---

## ✉️ Real-Time Email Classification

Users can input a custom email, and the model predicts the class based on probability scores.

The final classification is based on the **highest probability score**.

---

## ✅ Features

- High accuracy spam detection
- Zero false positives
- Probability-based prediction
- Real-time user input support
- Clean and optimized preprocessing pipeline

---

## 🔮 Future Improvements

- Try advanced models such as **Naive Bayes**, **SVM**, or **Neural Networks**
- Improve recall while maintaining low false positives
- Deploy as a **web application**
- Extend classification to email subject + body
- Handle class imbalance more effectively

---

## 📌 Conclusion

This project demonstrates a **practical and safe spam email detection system** using machine learning.  
It focuses not only on accuracy but also on **real-world reliability**, ensuring legitimate emails are not wrongly classified as spam.
