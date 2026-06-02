# Diabetes Risk Prediction Using Machine Learning

This repository contains a complete Machine Learning workflow implemented in a Jupyter Notebook to predict the risk of diabetes in patients based on specific medical and clinical measurements.

## 📋 Table of Contents
- [Project Overview](#-project-overview)
- [Dataset Summary](#-dataset-summary)
- [Project Architecture](#-project-architecture)
- [Installation & Prerequisites](#-installation--prerequisites)
- [How to Run](#-how-to-run)
- [Model Evaluation](#-model-evaluation)
- [License](#-license)

---

## 🔍 Project Overview
The goal of this project is to build a diagnostic classification model capable of predicting whether or not a patient has diabetes. Using a supervised learning framework, the project explores historical health statistics to establish baseline predictors and applies a **Logistic Regression** classifier to deliver both predictions and interpretable risk probabilities.

---

## 📊 Dataset Summary
The classification task is built using a dataset (`diabetes.csv`) consisting of **768 instances** and **9 clinical attributes**:

| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| `Pregnancies` | Integer | Number of times pregnant |
| `Glucose` | Integer | Plasma glucose concentration a 2 hours in an oral glucose tolerance test |
| `BloodPressure` | Integer | Diastolic blood pressure (mm Hg) |
| `SkinThickness` | Integer | Triceps skin fold thickness (mm) |
| `Insulin` | Integer | 2-Hour serum insulin (mu U/ml) |
| `BMI` | Float | Body mass index (weight in kg/(height in m)^2) |
| `DiabetesPedigreeFunction` | Float | Genetic risk score calculated based on family history |
| `Age` | Integer | Age in years |
| `Outcome` | Integer (Binary) | **Target Variable:** `1` if diabetic, `0` if non-diabetic |

---

## 🛠 Project Architecture
The Jupyter Notebook processes the data science pipeline step-by-step through the following milestones:
1. **Environment Setup:** Importing core scientific libraries including `numpy`, `pandas`, `matplotlib`, and `scikit-learn`.
2. **Exploratory Data Analysis (EDA):** Inspecting structural summary statistics (`.describe()`) and verifying feature configurations (`.info()`).
3. **Data Splitting:** Partitioning the dataset into independent feature vectors ($X$) and the dependent target column ($Y$), followed by a train-test validation split.
4. **Model Training:** Fitting and optimizing a binary **Logistic Regression** model using the training subset.
5. **Evaluation Metrics:** Generating performance assessments, a confusion matrix, and an explicit classification report on unseen test data.

---

## 💻 Installation & Prerequisites

To execute this notebook locally, ensure you have Python 3.x installed along with the required dependencies.

1. **Clone this repository:**
   ```bash
   git clone [https://github.com/hemalathac15/diabetes-risk-prediction-using-ml.git](https://github.com/hemalathac15/diabetes-risk-prediction-using-ml.git)
   cd diabetes-risk-prediction-using-ml
   
2. **Set up a Virtual Environment (Recommended):**

Bash
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate

3. **Install Dependencies:** 

Bash
pip install numpy pandas matplotlib scikit-learn jupyter
🚀 How to Run
Place your dataset file named exactly as diabetes.csv into the root directory of the project.


How to run?
1. Place your dataset file named exactly as diabetes.csv into the root directory of the project.

2. Launch the Jupyter Notebook environment terminal:

Bash
jupyter notebook
3. Open Diabetes Risk Prediction Using Machine Learning.ipynb and run the notebook cells sequentially to observe data transformations, training steps, and results.

📈 Model Evaluation
The predictive performance evaluated on the isolated validation test set yielded the following results:

Performance Metrics:
Global Test Accuracy Score: ~70.13%

Confusion Matrix:
Plaintext
 [[81  19]
  [27  27]]
True Negatives (Class 0 predicted correctly): 81

True Positives (Class 1 predicted correctly): 27

Detailed Classification Report:
Plaintext
               precision    recall  f1-score   support

           0       0.75      0.81      0.78       100
           1       0.59      0.50      0.54        54

    accuracy                           0.70       154
   macro avg       0.67      0.65      0.66       154
weighted avg       0.69      0.70      0.70       154
