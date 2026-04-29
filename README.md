# 🩺 Healthcare Risk Prediction Using Machine Learning

<div align="center">

![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.x-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Gradio](https://img.shields.io/badge/Gradio-Deployed-FF7C00?style=for-the-badge&logo=gradio&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

**An end-to-end machine learning pipeline for predicting diabetes risk using patient healthcare data.**

</div>

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Business Problem](#-business-problem)
- [Dataset](#-dataset)
- [Project Workflow](#-project-workflow)
- [Exploratory Data Analysis](#-exploratory-data-analysis)
- [Machine Learning Models](#-machine-learning-models)
- [Model Performance](#-model-performance)
- [Deployment](#-deployment)
- [Project Structure](#-project-structure)
- [How to Run](#-how-to-run)
- [Tech Stack](#-tech-stack)

---


## 🔍 Overview

Diabetes is a chronic disease that affects millions globally and can lead to severe complications heart disease, kidney failure, nerve damage, and vision loss if not detected early. This project builds a **machine learning-powered prediction system** that identifies patients at risk of diabetes using medical and lifestyle data.

> **Goal:** Predict whether a patient is diabetic or non-diabetic using structured healthcare data, and deploy the model through an interactive web interface.

---

## 💼 Business Problem

Healthcare organizations struggle to proactively identify at-risk patients across large populations. Manual data analysis is:
- ⏳ Time-consuming
- ❌ Prone to human error
- 📉 Inconsistent across practitioners

This project proposes a **data-driven screening tool** that gives healthcare providers quick, automated risk assessments enabling timely intervention, better resource allocation, and improved patient outcomes.

---

## 📊 Dataset

| Property | Details |
|---|---|
| **Records** | ~18,000 patient entries |
| **Target Variable** | `Outcome` (1 = Diabetic, 0 = Non-Diabetic) |
| **Task Type** | Binary Classification |

### Features Used

| Category | Features |
|---|---|
| **Demographics** | Age, Gender, Country |
| **Clinical Measurements** | Glucose, Blood Pressure, BMI, Insulin, Skin Thickness, Cholesterol, HbA1c, Fasting Blood Sugar |
| **Lifestyle Factors** | Physical Activity Level, Smoking Status, Sleep Hours, Daily Steps, Screen Time, Water Intake |
| **Genetic** | Diabetes Pedigree Function, Pregnancies |

---

## 🔄 Project Workflow

```
Raw Data (CSV)
     │
     ▼
Data Preprocessing
 ├── Handle missing values
 ├── Remove inconsistencies
 └── Feature/target split
     │
     ▼
Exploratory Data Analysis
 ├── Distribution plots
 ├── Age vs Diabetes status
 └── Correlation heatmap
     │
     ▼
Model Training
 ├── Logistic Regression
 ├── Decision Tree
 └── Random Forest
     │
     ▼
Model Evaluation
 ├── Accuracy Score
 ├── Confusion Matrix
 └── Classification Report
     │
     ▼
Deployment (Gradio Interface)
```

---

## 📈 Exploratory Data Analysis

Key insights discovered during EDA:

- 📊 **Glucose levels** showed the strongest association with diabetic outcomes higher values strongly correlated with positive cases
- 🏋️ **BMI** and **age** were also among the top contributing factors
- 🔗 **Correlation heatmap** revealed that most features had low inter-correlation, reducing multicollinearity concerns
- 📅 Diabetes cases were relatively distributed across all age groups (18–79), with no single age group dominating

---

## 🤖 Machine Learning Models

### 1. Logistic Regression
A linear baseline model using the **sigmoid function** to output diabetes probability. Best for understanding which features linearly influence outcomes.

- ✅ Highly interpretable
- ✅ Efficient on structured tabular data
- ⚠️ Assumes linear feature relationships

### 2. Decision Tree
A rule-based model that recursively splits data on features like glucose, BMI, and blood pressure using **Gini impurity** / **information gain**.

- ✅ Fully interpretable (visualizable tree)
- ✅ Captures non-linear patterns
- ⚠️ Prone to overfitting on complex trees

**Top Features (Decision Tree):** Daily Steps · Fasting Blood Sugar · Cholesterol · Blood Pressure · Glucose

### 3. Random Forest
An ensemble of many decision trees, each trained on random data/feature subsets. Final prediction via **majority voting**.

- ✅ Reduces overfitting
- ✅ Captures complex feature interactions
- ✅ Provides robust feature importance scores

**Top Features (Random Forest):** Diabetes Pedigree Function · Glucose · Cholesterol · Daily Steps · Fasting Blood Sugar · Insulin

---

## 🏆 Model Performance

| Model | Accuracy |
|---|---|
| 🥇 **Logistic Regression** | **71.6%** |
| 🥈 **Random Forest** | **71.5%** |
| 🥉 Decision Tree | 58.7% |

```
Logistic Regression  ████████████████████████████░░░░░░░░░░░░  71.6%
Random Forest        ████████████████████████████░░░░░░░░░░░░  71.5%
Decision Tree        ████████████████████████░░░░░░░░░░░░░░░░  58.7%
```

> **Logistic Regression** and **Random Forest** significantly outperform the Decision Tree, with very similar accuracy to each other. The Decision Tree's lower score likely reflects overfitting to the training set.

---

## 🚀 Deployment

The best-performing model was deployed using **Gradio** — an open-source Python library for building quick ML demos.

### Features of the App:
- 🖥️ Interactive web UI — no coding required
- 🔢 Input sliders for all key health indicators (glucose, BMI, age, blood pressure, etc.)
- ⚡ Instant prediction: **Diabetic** or **Not Diabetic** with probability
- 📋 Prediction history table for reviewing past inputs
- 🌐 Shareable via public link

### Run the App:
Simply run the **Gradio cell** at the bottom of the Jupyter notebook — it launches the interface instantly in your browser (or generates a shareable public link).

---

## 📁 Project Structure

```
healthcare-risk-prediction/
│
├── 📓 Diabetes_Risk_Prediction.ipynb   # Main notebook (EDA + modeling + Gradio deployment)
├── 📄 Final_Report_Group_11.pdf        # Full project report
├── 📊 diabetes_dataset.csv             # Dataset (add to repo or link source)
└── 📝 README.md                        # You are here
```

---

## ⚙️ How to Run

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/healthcare-risk-prediction.git
cd healthcare-risk-prediction
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Launch the Notebook & Run the Gradio App
```bash
jupyter notebook Diabetes_Risk_Prediction.ipynb
```
Once the notebook is open, run all cells. The **Gradio interface** will launch automatically at the bottom — opening in your browser or generating a public shareable link.

### Requirements
```
pandas
numpy
matplotlib
seaborn
scikit-learn
gradio
jupyter
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| **Python 3.8+** | Core programming language |
| **Pandas / NumPy** | Data manipulation |
| **Matplotlib / Seaborn** | Data visualization |
| **Scikit-Learn** | ML model training & evaluation |
| **Gradio** | Model deployment & UI |
| **Jupyter Notebook** | Development environment |

---

<div align="center">

**⭐ If you found this project helpful, please give it a star!**

*Made with ❤️ for healthcare innovation through data science*

</div>
