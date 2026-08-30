# Accuracy Improvement Challenge in College Admission Prediction Model

## 📌 Project Overview
This project focuses on improving the performance of a baseline college admission prediction model developed during a class case study. The baseline Logistic Regression model was evaluated first, followed by experimentation with feature engineering and feature scaling techniques to identify an approach that could improve predictive accuracy.

The project emphasizes a comparative approach, where the baseline model and different improvement attempts are evaluated to determine the most effective technique.

---

## 🎯 Objective
The objective of this project is to improve the accuracy of the existing college admission prediction model by applying feature engineering, feature scaling, and model optimization techniques, while comparing the results against the original baseline model.

---

## 🛠 Tools & Technologies
- **Python**
- **Jupyter Notebook**
- **Pandas** – Data manipulation and preprocessing
- **NumPy** – Numerical operations
- **Matplotlib** – Visualization
- **Seaborn** – Visualization
- **Scikit-learn** – Machine learning and model evaluation

### Techniques & Models Used
- Logistic Regression
- Feature Engineering
- StandardScaler
- GridSearchCV
- Train-Test Split
- Model Accuracy Comparison

---

## 📂 Dataset
The project uses the **same college admission dataset used in the class case study**, as required for the accuracy improvement challenge.

The dataset contains academic and institutional features used to predict whether a student is admitted.

### Main Features
- **GRE (`gre`)** – Graduate Record Examination score
- **GPA (`gpa`)** – Grade Point Average
- **University Rank (`rank`)** – Ranking category of the applicant's university
- **Admission (`admit`)** – Target variable indicating admission outcome

The target variable represents a binary classification problem:
```text
1 → Admitted
0 → Not Admitted
```

---

## 🔄 Project Workflow

```text
Class Case Study Dataset
  ↓
Initial Data Exploration
  ↓
Baseline Logistic Regression
  ↓
Baseline Accuracy
  ↓
Feature Engineering
  ↓
Evaluate Accuracy
  ↓
Feature Scaling
  ↓
Improved Logistic Regression
  ↓
Compare Results
  ↓
Calculate Accuracy Improvement
  ↓
Interpret Results
```

---

## 📊 Baseline Model
The original class case study was used as the starting point for the project. A Logistic Regression model was trained using the original features and evaluated using a train-test split.

**Baseline Accuracy: 66.25%**

This baseline serves as the reference point against which all improvement attempts were compared.

---

## 🔧 Improvement Attempt 1 – Feature Engineering
A new interaction feature called `GRE_GPA` was created:

```text
GRE_GPA = gre × gpa
```

The purpose of this feature was to capture the combined effect of GRE score and GPA rather than considering the two variables independently.

**Result**
The model accuracy decreased from:
- Baseline Accuracy = 66.25%
- Feature Engineering Accuracy = 63.75%

This represents a relative accuracy change of approximately **-3.77%**.

**Interpretation**
The engineered interaction feature did not provide additional useful predictive information for this dataset and slightly reduced model performance. This experiment demonstrated that adding a new feature does not necessarily improve a model and that feature usefulness should be validated empirically.

---

## ⚙️ Improvement Attempt 2 – Feature Scaling
Feature scaling was then applied using `StandardScaler` before training Logistic Regression. Scaling was performed to bring the numerical input features to a comparable scale and allow the Logistic Regression algorithm to optimize its parameters more effectively.

**Result**
The scaled Logistic Regression model achieved:
- Improved Accuracy = 67.50%

This was higher than the baseline accuracy of 66.25%.

---

## 📈 Model Comparison

| Approach | Accuracy |
|---|---|
| Baseline Logistic Regression | 66.25% |
| Logistic Regression + Feature Engineering | 63.75% |
| Logistic Regression + Feature Scaling | 67.50% |

The comparison shows that feature engineering alone reduced the model's performance, whereas feature scaling produced the best result among the approaches tested.

---

## 📊 Accuracy Improvement
The percentage improvement was calculated relative to the baseline model:

```text
Accuracy Improvement = ((Improved Accuracy - Baseline Accuracy) / Baseline Accuracy) × 100
```

Using the obtained results:
- Baseline Accuracy = 66.25%
- Improved Accuracy = 67.50%
- **Accuracy Improvement ≈ 1.89%**

Therefore, the final model achieved an approximate **1.89% improvement** in accuracy over the baseline Logistic Regression model.

---

## 🔍 Key Insights
- The baseline Logistic Regression model achieved an accuracy of 66.25%.
- The engineered `GRE_GPA` interaction feature reduced accuracy to 63.75%, indicating that the additional feature did not improve predictive performance.
- Feature scaling using StandardScaler improved the Logistic Regression model's accuracy to 67.50%.
- The final model achieved a 1.89% relative improvement over the baseline.
- The results demonstrate that preprocessing techniques can have a measurable effect on machine learning performance.
- The project also highlights the importance of testing and comparing different approaches rather than assuming that additional features or more complex processing will always improve accuracy.

---

## 💼 Practical Implications
An admission prediction model can be used as a decision-support tool to help institutions estimate admission outcomes based on academic indicators such as GRE score, GPA, and university rank.

A model with improved predictive performance can assist in screening applications more efficiently and support data-driven admission analysis. However, predictions should be considered as an additional analytical input rather than a replacement for institutional admission policies and human judgment.

---

## 📁 Project Structure
Accuracy-Improvement-Challenge-in-College-Admission-Prediction-Model/
│
├── College_admission_Prediction.ipynb
├── README.md
└── college_admission.csv

---

## 🚀 How to Run the Project

1. Clone the repository
```bash
   git clone https://github.com/omhunagund/Accuracy-Improvement-Challenge-in-College-Admission-Prediction-Model.git
```
2. Navigate to the project directory
```bash
   cd Accuracy-Improvement-Challenge-in-College-Admission-Prediction-Model
```
3. Install the required libraries
```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```
4. Launch Jupyter Notebook
```bash
   jupyter notebook
```
5. Open the notebook
   Open `College_admission_Prediction.ipynb` and execute the cells sequentially.

---

## ✅ Project Outcome
The project successfully compared the original baseline admission prediction model with multiple improvement attempts. Although the feature-engineering approach decreased accuracy, feature scaling improved Logistic Regression performance from 66.25% to 67.50%, resulting in a 1.89% relative improvement over the baseline.

The project demonstrates the importance of experimentation, preprocessing, and quantitative comparison when improving machine learning model performance.

---

## 👤 Author
**Om Hunagund**
GitHub: [github.com/omhunagund](https://github.com/omhunagund)