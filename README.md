# Diabetes Prediction

A machine learning project that predicts whether a patient is likely to have diabetes based on diagnostic health measurements.

---

## The Problem

Diabetes is one of the fastest-growing chronic diseases globally, and early detection can significantly change outcomes. This project explores whether a trained ML model — given a few basic health indicators — can flag high-risk individuals before clinical diagnosis.

---

## Dataset

**Pima Indians Diabetes Dataset** (via Kaggle / UCI Machine Learning Repository)

- 768 patient records
- 8 input features: Pregnancies, Glucose, Blood Pressure, Skin Thickness, Insulin, BMI, Diabetes Pedigree Function, Age
- Binary target: Diabetic (1) or Not Diabetic (0)

---

## What I did

- Handled zero-value anomalies in Glucose, BMI, and Blood Pressure (these can't be 0 biologically — replaced with column medians)
- Performed exploratory data analysis to understand feature distributions and class imbalance
- Standardized features using `StandardScaler` before model training
- Trained and evaluated multiple classifiers, selecting the best performer

---

## Tech Stack

| Tool | Purpose |
|---|---|
| Python | Core language |
| Pandas & NumPy | Data manipulation |
| Matplotlib & Seaborn | Visualization |
| Scikit-learn | Model training & evaluation |
| Jupyter Notebook | Development environment |

---

## Results

| Metric | Score |
|---|---|
| Model | Support Vector Machine (SVM) |
| Training Accuracy | ~78% |
| Test Accuracy | ~77% |

The model correctly identifies diabetic patients at a reasonable rate given the dataset size and class imbalance.

---

## How to run

```bash
git clone https://github.com/manishbhatt1/Diabetes_Prediction.git
cd Diabetes_Prediction
pip install pandas numpy matplotlib seaborn scikit-learn
jupyter notebook Diabetes_Prediction.ipynb
```

---

## Key takeaways

Glucose level and BMI turned out to be the strongest predictors — which aligns with clinical understanding. The bigger challenge was handling missing/zero values intelligently rather than just dropping rows.
