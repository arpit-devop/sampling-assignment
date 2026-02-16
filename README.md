

# 📊 Impact of Sampling Techniques on Imbalanced Credit Card Dataset

## 📌 Project Overview

Class imbalance is a major challenge in real-world machine learning applications such as fraud detection. In highly imbalanced datasets, models often achieve misleadingly high accuracy by favoring the majority class while failing to correctly classify minority instances.

This project evaluates the impact of five different sampling techniques on five machine learning models using a credit card fraud dataset. The objective is to determine which sampling strategy performs best for each model.

---

## 🎯 Objectives

* Convert a highly imbalanced dataset into balanced datasets.
* Apply five distinct sampling techniques.
* Train five machine learning models.
* Compare accuracy across all combinations.
* Identify the best sampling technique for each model.

---

## 📂 Dataset

**Dataset:** Credit Card Fraud Dataset
Source:
[https://github.com/AnjulaMehto/Sampling_Assignment/blob/main/Creditcard_data.csv](https://github.com/AnjulaMehto/Sampling_Assignment/blob/main/Creditcard_data.csv)

### Dataset Characteristics:

* Binary Classification Problem
* Target Column: `Class`

  * `0` → Non-Fraud
  * `1` → Fraud
* Highly imbalanced class distribution

---

## ⚖️ Sampling Techniques Used

| Sampling ID | Technique             | Category               |
| ----------- | --------------------- | ---------------------- |
| Sampling1   | Random Over Sampling  | Oversampling           |
| Sampling2   | Random Under Sampling | Undersampling          |
| Sampling3   | SMOTE                 | Synthetic Oversampling |
| Sampling4   | NearMiss              | Undersampling          |
| Sampling5   | SMOTEENN              | Hybrid (Over + Under)  |

---

## 🤖 Machine Learning Models

| Model ID | Algorithm                    |
| -------- | ---------------------------- |
| M1       | Logistic Regression          |
| M2       | Decision Tree                |
| M3       | Random Forest                |
| M4       | Support Vector Machine (SVM) |
| M5       | K-Nearest Neighbors (KNN)    |

---

## 🧪 Experimental Setup

1. The dataset was first analyzed for imbalance.
2. Each sampling technique was applied separately.
3. Data was split into 70% training and 30% testing.
4. Each model was trained on each sampled dataset.
5. Accuracy was computed and compared.

---

## 📊 Accuracy Results (%)

| Model                        | Random Over | Random Under | SMOTE | NearMiss | SMOTEENN  |
| ---------------------------- | ----------- | ------------ | ----- | -------- | --------- |
| **M1 – Logistic Regression** | 91.92       | 33.33        | 90.83 | 50.00    | **97.07** |
| **M2 – Decision Tree**       | 98.91       | 33.33        | 97.16 | 16.67    | **99.71** |
| **M3 – Random Forest**       | **100.00**  | 16.67        | 99.13 | 16.67    | 100.00    |
| **M4 – SVM**                 | **73.80**   | 16.67        | 68.56 | 16.67    | 73.02     |
| **M5 – KNN**                 | **98.47**   | 50.00        | 81.88 | 83.33    | 95.60     |

---

## 🏆 Best Sampling Technique for Each Model

* **Logistic Regression (M1)** → SMOTEENN (97.07%)
* **Decision Tree (M2)** → SMOTEENN (99.71%)
* **Random Forest (M3)** → Random Over Sampling (100%)
* **SVM (M4)** → Random Over Sampling (73.80%)
* **KNN (M5)** → Random Over Sampling (98.47%)

---

## 🔍 Key Observations

1. Random Under Sampling significantly reduced model performance due to information loss.
2. NearMiss also performed poorly across most models.
3. SMOTEENN (Hybrid technique) achieved the highest accuracy for Logistic Regression and Decision Tree.
4. Random Over Sampling performed exceptionally well with Random Forest and KNN.
5. Random Forest showed the most robust performance overall, achieving 100% accuracy with two sampling techniques.
6. Sampling technique selection greatly influences classification performance.

---

## 📈 Discussion

The experiment clearly demonstrates that:

* Imbalanced datasets negatively impact model generalization.
* Oversampling techniques are generally more effective than undersampling.
* Hybrid techniques (SMOTEENN) provide improved balance while reducing noise.
* Ensemble methods (Random Forest) are more resilient to imbalance.
* There is no universally best sampling technique — performance depends on the model used.

---

## 🛠️ Technologies Used

* Python 3
* Pandas
* NumPy
* Scikit-learn
* Imbalanced-learn
* Google Colab

---



## ▶️ How to Run

1. Clone the repository
2. Install dependencies

   ```
   pip install -r requirements.txt
   ```
3. Run the notebook/script in Google Colab or local environment

---

## 📌 Conclusion

This study highlights the critical importance of applying appropriate sampling techniques when working with imbalanced datasets. The results confirm that oversampling and hybrid approaches significantly improve model performance compared to pure undersampling methods.

Choosing the correct sampling strategy is essential for building reliable fraud detection systems.

---

## 👨‍💻 Author

Arpit Agarwal
B.Tech – Predictive Analytics


