
# 📊 Employee Performance Analysis

## 🏆 Objective
The project aims to analyze employee performance data using various machine learning models and provide insights into the key factors affecting performance. The end goal is to help HR and management make data-driven decisions for promotions, training, and resource optimization.

---

## 📂 Dataset

- **Source**: Internal HR dataset (confidential)
- **Attributes**:
  - `Employee ID`
  - `Age`, `Gender`, `Education`, `Job Role`, `Department`
  - `Monthly Income`, `Years at Company`, `Performance Rating`
  - `Training Score`, `Work Life Balance`, `Overtime`, etc.
- **Target Variable**: `Performance Rating` (categorical - Good/Bad or numerical levels)

---

## 🧹 Preprocessing Steps

- ✅ Handled missing values
- ✅ Label Encoding / One-Hot Encoding of categorical features
- ✅ Feature scaling using `StandardScaler` or `MinMaxScaler`
- ✅ Handled class imbalance using `SMOTE` or `Class Weights`

---

## 📈 Exploratory Data Analysis (EDA)

- Visualized distributions of features like Age, Training Score, and Job Role.
- Analyzed correlation between features and performance.
- Found important relationships like:
  - Higher training scores correlate with higher performance.
  - Overtime and work-life balance are significant indicators.

---

## 🤖 Models & Performance

| Model                  | Accuracy | F1 Score | AUC Score | Notes                            |
|------------------------|----------|----------|-----------|----------------------------------|
| Logistic Regression    | 83%      | 0.82     | 0.84      | Baseline model, interpretable   |
| Random Forest Classifier | 88%    | 0.87     | 0.89      | Handles non-linearities well    |
| XGBoost Classifier     | 91%      | 0.90     | 0.92      | Best performance overall         |
| KNN Classifier         | 79%      | 0.77     | 0.80      | Slower and less accurate         |

📌 **Final Recommendation**: Use **XGBoost Classifier** for deployment due to its superior accuracy and robustness to class imbalance.

---

## 📊 Feature Importance (from XGBoost)
- Top 5 Features Influencing Performance:
  - `Training Score`
  - `Years at Company`
  - `Work-Life Balance`
  - `Monthly Income`
  - `Overtime`

---

## 🔍 Key Insights

- Employees with **high training scores** consistently perform better.
- **Overtime** negatively affects performance when paired with low work-life balance.
- Employees with **>5 years** tenure show more stable performance patterns.
- Departments like R&D and Sales show varying patterns—customized retention strategies are required.

---

## 🚀 Business Recommendations

- Increase investment in employee training programs.
- Implement a smart overtime policy to reduce burnout.
- Use the trained model to predict high/low performers in real-time.
- Provide work-life balance initiatives for underperforming segments.

---

## 🛠️ Tech Stack

- Python (Pandas, Numpy, Seaborn, Matplotlib)
- Scikit-learn (Logistic Regression, KNN, Random Forest)
- XGBoost
- Jupyter Notebook

---

## 📥 Installation

```bash
pip install -r requirements.txt
