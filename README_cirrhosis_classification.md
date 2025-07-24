
# 🧬 Cirrhosis Survival Prediction — Classification Model

## 📌 Project Overview
This machine learning classification project is focused on predicting the survival status of patients with cirrhosis. Using a variety of clinical features, the model aims to support early prognosis and aid healthcare professionals in risk assessment.

---

## 🗂️ Dataset Information
- **File**: `train.csv` and `test.csv`
- **Rows in training set**: 15,000
- **Columns**: 20
- **Target Variable**: `Status`
  - `C`: Continue (still alive)
  - `CL`: Complications or progression
  - `D`: Dead
- **Missing Values**: Present in `Cholesterol`, `Drug`, `Tryglicerides`, etc.
- **Feature Types**:
  - Categorical: `Drug`, `Sex`, `Ascites`, `Hepatomegaly`, `Spiders`, `Edema`, `Status`
  - Numerical: `Age`, `Bilirubin`, `Albumin`, `Prothrombin`, `Cholesterol`, etc.

---

## ⚙️ Preprocessing Steps
- Categorical encoding using `LabelEncoder` / `OneHotEncoder`
- Missing value imputation using `SimpleImputer` (mean strategy)
- Train-Test split (80/20 and 70/30 tested)
- Feature scaling (if applicable)

---

## 🤖 Models Implemented
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree
- Random Forest
- Support Vector Classifier (SVC)
- XGBoost Classifier

---

## 🏆 Best Performing Model

**Random Forest Classifier** provided the most balanced results in terms of accuracy and F1-score:

- Accuracy: **84.83%**
- Macro F1-score: **0.57**
- Weighted F1-score: **0.85**
- Precision: **0.85**
- Recall: **0.85**

Even though XGBoost slightly outperformed in raw accuracy (85.06%), Random Forest showed better class-wise F1 and stability.

---

## 📊 Evaluation & Visualizations
- Confusion matrices for all models
- Precision, Recall, F1-score bar comparison
- ROC curves (if applicable)
- Heatmap and correlation plots

---

## 📦 Final Prediction on Test Data
- Final test set size: 10,000 patients
- Models were used to predict probabilities (`predict_proba`)
- Submission file format:

```
| id    | Status_C | Status_CL | Status_D |
|-------|----------|-----------|----------|
| 15000 | 0.41     | 0.001     | 0.58     |
| 15001 | 0.94     | 0.006     | 0.05     |
...
```

The submission was saved as `submission.csv` using:

```python
submission.to_csv('submission.csv', index=False)
```

---

## 🧰 Technologies Used
- Python
- pandas, numpy
- matplotlib, seaborn
- scikit-learn
- xgboost

---

## 📈 Future Improvements
- Use of SMOTE or class weighting for minority class recall
- SHAP or LIME explainability
- Hyperparameter tuning (GridSearchCV)
- Streamlit-based medical interface for doctors

---

## 🚀 How to Run

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
pip install -r requirements.txt
jupyter notebook
```

---

## 📄 License
MIT License
