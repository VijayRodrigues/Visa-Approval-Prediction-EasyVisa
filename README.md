# 🛂 Visa Approval Prediction - EasyVisa

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
- Evaluated models using **accuracy, F1-score, confusion matrix**, etc.
- Deployed the final model using `joblib` for real-world inference.

---

## 🛠 Tools & Technologies

- **Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)**
- **Machine Learning: Decision Tree, Random Forest, XGBoost, etc.**
- **Model Tuning: GridSearchCV / RandomizedSearchCV**
- **Model Saving: `joblib`**
- **Jupyter Notebook** for experiments

---

## 📈 Outcome

- Designed an automated prediction pipeline.
- Improved processing time and decision quality for visa applications.
- Identified key drivers such as **education**, **experience**, **wage**, and **full-time status** as major influencers of visa approval.

---

## 💾 Repository Structure

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
