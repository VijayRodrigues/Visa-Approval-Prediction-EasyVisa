# 🛂 Visa Approval Prediction - EasyVisa x OFLC

## 📘 Project Context

Business communities in the United States are continuously seeking skilled professionals to meet growing labor demands. To fulfill these gaps, the **Immigration and Nationality Act (INA)** allows foreign workers to be employed temporarily or permanently, while ensuring the protection of U.S. workers' wages and working conditions.

The **Office of Foreign Labor Certification (OFLC)** oversees this process and in **FY 2016 alone, processed 775,979 employer applications** for nearly **1.7 million positions**. However, the manual process of reviewing every case has become increasingly complex and time-consuming.

To address this, OFLC partnered with **EasyVisa**, a data-driven firm, to automate and optimize the visa certification process using **machine learning techniques**.

---

## 🎯 Objective

As a Data Scientist at EasyVisa, the task is to develop a **classification model** to:

- 🔍 Predict whether a visa will be **certified or denied**.
- 🤖 Automate and accelerate the decision-making process for visa applications.
- 📊 Identify key drivers that influence visa approval.
- 💡 Recommend suitable applicant profiles for approval or denial.

---

## 📂 Dataset Overview

The dataset includes diverse features related to employees and employers, offering a real-world glimpse into the visa certification ecosystem.

### 📋 Feature Description

| Feature                  | Description |
|--------------------------|-------------|
| `case_id`               | Unique ID for each visa application |
| `continent`             | Continent of origin of the applicant |
| `education_of_employee` | Educational background of the employee |
| `has_job_experience`    | Does the employee have prior job experience? (Y/N) |
| `requires_job_training` | Does the employee need job training? (Y/N) |
| `no_of_employees`       | Number of employees in the employer's company |
| `yr_of_estab`           | Year the employer’s company was established |
| `region_of_employment`  | Intended employment region in the U.S. |
| `prevailing_wage`       | Average wage offered for the job |
| `unit_of_wage`          | Wage unit (Hourly, Weekly, Monthly, Yearly) |
| `full_time_position`    | Is the job full-time? (Y/N) |
| `case_status`           | Target Variable: Visa `Certified` or `Denied` |

---

## 🧠 Machine Learning Approach

- Performed **Exploratory Data Analysis (EDA)** to uncover insights.
- Built various **classification models** to predict visa outcomes.
- Used **GridSearchCV** and **RandomizedSearchCV** for hyperparameter tuning.
- Evaluated models using **accuracy, F1-score, precision, recall, ROC-AUC**, etc.
- Deployed the final model using `joblib` for real-world inference.

---

## 🛠 Tools & Technologies

- **Python**: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
- **ML Models**: Decision Tree, Random Forest, Bagging, Gradient Boosting
- **Tuning**: GridSearchCV, RandomizedSearchCV
- **Notebook**: Jupyter for analysis and experimentation

---

## 📈 Actionable Insights & Recommendations

### 🔄 Bagging Models

#### ✅ Tuned `BaggingClassifier` (Best Performer)

- **Highest Accuracy & ROC-AUC**: Among all models, Tuned Bagging showed the best predictive performance.
- **Balanced Report**: Well-distributed precision, recall, and F1-scores across both classes.
- **Slightly Outperformed Random Forest**: Marginally better results than Tuned Random Forest.
- **Highlight**: Hyperparameter tuning made a significant difference in model performance.

### 🚀 Boosting Models

#### ✅ Tuned `GradientBoostingClassifier`

- **Accuracy & ROC-AUC**: Achieved **0.7714 accuracy** and **0.8600 ROC-AUC** – highest among all models.
- **Consistent Metrics**: Delivered strong precision, recall, and F1-scores across both classes.
- **Better Weighted Averages**: Excellent performance even with class imbalance.
- **Conclusion**: The best choice for real-world deployment due to its consistent performance across all metrics.

---

## 💼 Business Takeaways

- 🌏 **Focus on Asian Regions**: Applicants from Asia form a large portion of approved candidates; recruiting efforts can be intensified here.
- 📍 **Southern U.S. Advantage**: Higher visa approval rates noted in Southern regions (e.g., Texas); local labor shortages may be favorable for foreign hiring.
- 💼 **Permanent Positions Preferred**: Candidates applying for permanent roles have a higher approval rate than those applying for contract jobs.
- 🎓 **Higher Education Pays Off**: Applicants with **Master’s degrees or above** are more likely to get approvals. Educational attainment is a strong predictor of success.
- 📊 **Data-Driven Shortlisting**: The company can implement this model into their recruitment pipeline for quicker, more accurate decisions.

---

## 🗂 Repository Structure

```bash
📁 visa-approval-prediction/
├── 📊 EDA_and_Preprocessing.ipynb
├── 🤖 Model_Training_and_Evaluation.ipynb
├── ✅ Final_Model_Pipeline.ipynb
├── 📁 data/
│   └── visa_data.csv
├── 📁 models/
│   └── easyvisa_model.pkl
└── README.md
