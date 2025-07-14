# 🫀 CardioRisk: A Data-Driven Machine Learning Model for Predicting Heart Disease

## 📖 Project Overview
CardioRisk is a comprehensive end-to-end data science project that analyzes the **Heart Disease Dataset (2020)** using statistical techniques, data visualization, and supervised machine learning models to **identify key health risk factors** and **predict heart disease**. Special attention is given to **class imbalance** using **SMOTE**, leading to significantly improved recall and overall model performance.

---

## 🌐 Dataset Information
- **Source:** [CDC Behavioral Risk Factor Surveillance System (BRFSS) 2020]
- **Size:** 319,000+ records, 17 features
- **Target Variable:** HeartDisease (1 = Yes, 0 = No)
- **Features:** Demographics, medical conditions, lifestyle habits (e.g., smoking, alcohol use, sleep, activity level)

---

## 🔎 Project Highlights

### ✅ Data Preprocessing
- Cleaned dataset and converted categorical values to numerical formats
- One-hot encoded categorical features for ML compatibility
- Addressed **class imbalance** using **SMOTE (Synthetic Minority Over-sampling Technique)**

### 📊 Exploratory Data Analysis (EDA)
- Explored feature distributions and interactions using Seaborn & Matplotlib
- Found strong associations between **diabetes**, **stroke**, **difficulty walking**, and heart disease

### 🧪 Statistical Hypothesis Testing
- Performed **Shapiro-Wilk normality tests** (most features were non-normal)
- Used **Chi-square tests** to identify statistically significant relationships between categorical variables and the heart disease outcome
- Generated a **correlation heatmap** to understand feature relationships

### 🧠 Machine Learning Models Used
| Model                | Accuracy | Precision | Recall | F1-score |
|---------------------|----------|-----------|--------|----------|
| Logistic Regression | ~91.2%   | 0.54      | 0.09   | 0.15     |
| Extra Trees         | ~89.3%   | 0.31      | 0.15   | 0.20     |
| KNN                 | ~90.3%   | 0.33      | 0.08   | 0.12     |
| XGBoost (final)     | **92.2%**| **0.96**  | **0.88** | **0.92** |

> Final model trained with **XGBoost + SMOTE** achieved the best F1-score and recall, making it ideal for identifying high-risk individuals.

### 📈 Final Classification Report
- ✅ **Accuracy:** 92.2%
- ✅ **Precision:** 95.7%
- ✅ **Recall:** 88.4%
- ✅ **F1-score:** 91.9%
- 🧮 **Confusion Matrix**:  
  [[28166, 1135],  
   [3382, 25802]]

---

## 💡 Key Insights
- **Diabetes, stroke history, poor general health**, and **difficulty walking** were among the **top predictors** of heart disease.
- Significant **class imbalance** initially led to misleading accuracy; handled using **SMOTE** to improve recall.
- Recall is crucial for medical predictions as **false negatives can be life-threatening**.

---

## 🩺 Real-World Implications
- Predictive models like this can be used in **clinical risk scoring**, **preventive screening programs**, or **digital health apps**.
- Identifies individuals at high risk who may benefit from **early intervention** or **lifestyle changes**.

---

## 💻 Technologies Used
- Python (Pandas, NumPy)
- Visualization: Matplotlib, Seaborn
- Statistical Testing: SciPy
- Machine Learning: Scikit-Learn, XGBoost
- Class Balancing: imbalanced-learn (SMOTE)
- Jupyter Notebook / Google Colab

---

## 🚀 How to Run

1. Clone the repo:
```bash
git clone https://github.com/624mihir/CardioRisk.git
cd CardioRisk

2. Install required libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost imbalanced-learn

3. Run the notebook:
- Open cardioRisk.ipynb in Jupyter or Google Colab.
- Run all cells sequentially


