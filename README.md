# 🎓 Student Performance Prediction using Machine Learning

This project leverages machine learning techniques to predict academic performance based on various student-related attributes such as study habits, attendance, extracurricular involvement, and parental support.

## 🧠 Project Objective
The goal is to build a classification model that accurately predicts students' final grade categories (`GradeClass`) using input features like:
- Study time per week
- Number of absences
- Participation in extracurricular activities
- Parental support level
- GPA

## 📁 Dataset
- Name: **Student Performance Prediction**
- Format: CSV
- Type: Tabular dataset containing numeric encodings of demographic and behavioral attributes.

## 🔍 Exploratory Data Analysis (EDA)
- Age is centered around 15–18 years.
- Study time is mostly around 10 hours/week.
- GPA has a strong positive correlation (0.78) with final grades.
- Absences negatively correlate with GPA (-0.92).
- Gender, sports, music, and volunteering showed minimal correlation with grades and were excluded from model training.

## 📊 Key Insights
- Students with more parental support and fewer absences tend to perform better.
- Female students generally study more than males.
- Higher GPA is more common among students with strong parental support.
- Extracurricular activity involvement is inversely correlated with academic performance.

## 🧹 Preprocessing
- Dropped irrelevant features: `StudentID`, `Music`, `Sports`, `Volunteering`.
- Standardized numerical columns using `StandardScaler`.
- Target variable: `GradeClass`
- Train-test split: **80/20**

## 🤖 Models Used
Nine classification models were trained and evaluated:
1. K-Nearest Neighbors
2. Support Vector Machine
3. Logistic Regression
4. Decision Tree
5. Random Forest ✅
6. Gradient Boosting
7. AdaBoost
8. Gaussian Naive Bayes
9. XGBoost ✅

## 📈 Results
- **Random Forest** achieved the highest accuracy: **91.65%**
- **XGBoost** was also a top performer.
- These two models were selected for further tuning and evaluation.

## ⚙️ Hyperparameter Tuning
**GridSearchCV** was used for optimal tuning:

**Random Forest**
- `n_estimators`: 100
- `max_depth`: 10
- `min_samples_split`: 5

**XGBoost**
- `n_estimators`: 50
- `max_depth`: 3
- `learning_rate`: 0.1

## 🧪 Evaluation Metrics
Models were evaluated on:
- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

Visualization includes:
- ROC curves for all models
- Bar plots comparing Precision, Recall, and F1-Score

## 📊 Feature Importance
Features with highest importance (from Random Forest):
- GPA
- Absences
- Parental Support
- Study Time

## 📌 How to Run
1. Open the Colab notebook: **`student_performance_ml.ipynb`**
2. Upload the dataset or use a path to the provided CSV.
3. Run all cells sequentially.

## 📎 Future Work
- Deployment as a web app or dashboard
- Incorporation of temporal performance data
- Multiclass classification improvement

---

> 📂 Repository includes:
> - `student_performance_ml.ipynb` – Full pipeline notebook
> - `student_performance.py` – Python version of the notebook (optional)
> - `README.md` – Project documentation

---

### 📬 Contact
For queries, reach out via LinkedIn.

