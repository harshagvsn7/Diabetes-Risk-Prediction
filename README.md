
# 🩺 Diabetes Risk Prediction Using Machine Learning

> End to end machine learning project to predict diabetes risk using healthcare data, with deployment using Gradio.

---

## 📌 Overview

This project focuses on predicting diabetes risk using machine learning techniques applied to healthcare data.

It covers the full pipeline from data preprocessing and exploratory analysis to model building, evaluation, and deployment as an interactive application.

---

## 🎯 Problem Statement

Develop a machine learning model that predicts whether a patient is likely to have diabetes based on medical and lifestyle features such as glucose level, BMI, age, and physical activity.

---

## 📊 Dataset

* ~18,000 patient records 

* Features include:

  * Age
  * Gender
  * BMI
  * Glucose level
  * Blood pressure
  * Insulin
  * Physical activity
  * Smoking status
  * Sleep hours

* Target variable:

  * 1 → Diabetic
  * 0 → Non Diabetic

---

## 🛠️ Tech Stack

* Python
* pandas, numpy
* matplotlib, seaborn
* scikit-learn
* Gradio

---

## 🔍 Data Preprocessing

* Removed missing values
* Cleaned inconsistent data
* Feature and target split
* Train test split

---
## 📈 Exploratory Data Analysis

* Analyzed feature distributions
* Identified trends and patterns
* Used visualizations for better understanding
* Performed correlation analysis

---


## 📊 Key Insights

* Glucose level is the strongest predictor of diabetes 
* BMI and age also have significant impact 
* Both medical and lifestyle factors influence prediction

---

## 🤖 Models Used

* Logistic Regression
* Decision Tree
* Random Forest

---

## 📊 Model Performance

| Model               | Accuracy |
| ------------------- | -------- |
| Logistic Regression | 0.716    |
| Decision Tree       | 0.587    |
| Random Forest       | 0.715    |

(Logistic Regression performed best, closely followed by Random Forest) 

---

## 📉 Feature Importance

Random Forest shows:

* Diabetes pedigree function
* Glucose
* Cholesterol
* Daily steps

as top contributing features (see report page 13).

---

## 🌐 Deployment

The model is deployed using **Gradio**.

* Users input patient details
* Model predicts diabetes risk instantly
* Works as an interactive interface

<img width="900" height="435" alt="image" src="https://github.com/user-attachments/assets/ffd29b23-cb9a-4e92-a448-fd6cee19612b" />


---

## 🔗 Live Demo

For demo just run the notebook, then it in the end it shows the link as https:://1270.xxxx.xxxx something like this and click on the link it popups to browser directly.
Do the rest of part like to predict or check them by putting the inputs.

---

## ⚙️ How to Run

```bash
# Clone repository
git clone https://github.com/your-username/healthcare-risk-prediction.git

cd healthcare-risk-prediction

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn gradio

# Run notebook
jupyter notebook "Capstone 2 Final.ipynb"

# Run app
python app.py
```

---

## 📂 Project Structure

```plaintext
healthcare-risk-prediction/
│── Capstone 2 Final.ipynb
│── app.py
│── dataset.csv
│── README.md
│── LICENSE
```

---

## 🚀 Project Status

* Completed data preprocessing
* Performed EDA with visual insights
* Built and compared ML models
* Achieved ~71% accuracy
* Deployed using Gradio

---

## 🔮 Possible Extensions

* Improve UI design
* Add input validation
* Use larger datasets
* Improve model performance

---

## 📄 License

MIT License

Copyright (c) 2026 Your Name

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files to deal in the Software
without restriction, including without limitation the rights to use, copy,
modify, merge, publish, distribute, sublicense, and or sell copies of the Software.

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND.


---

## ⭐ Support

Give it a star if you found it useful.

