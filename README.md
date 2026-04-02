# Stroke Prediction Analysis: Handling Imbalanced Healthcare Data

## 📌 Project Overview
This project aims to predict the likelihood of a patient having a stroke based on demographic and clinical features (e.g., age, hypertension, heart disease, BMI, and smoking status). 

Predicting strokes is a critical healthcare challenge, further complicated by **extreme class imbalance**, as stroke cases typically represent a very small fraction (~5%) of the total population in the dataset.

## 🛠️ Methodology
To build a robust and reliable predictive system, the following pipeline was implemented:

1.  **Data Preprocessing**: 
    *   Handled missing values in `BMI` using median imputation.
    *   Feature scaling for numerical data and One-Hot Encoding for categorical features.
    *   Automated the workflow using Scikit-Learn `Pipeline` and `ColumnTransformer` for reproducibility.
2.  **Imbalance Management**: 
    *   Applied **SMOTE (Synthetic Minority Over-sampling Technique)** to balance the training set, allowing the models to learn patterns from the minority class effectively.
3.  **Model Evaluation**: 
    *   Compared multiple algorithms: Logistic Regression and Random Forest.
    *   Prioritized **F1-Score** and **Recall** over Accuracy due to the imbalanced nature of the target variable.

## 📈 Key Results

| Model | Accuracy | F1-Score | AUC |
| :--- | :--- | :--- | :--- |
| Logistic Regression (Baseline) | 0.63 | 0.24 | 0.84 |
| **Logistic Regression (Optimized)** | **0.91** | **0.37** | **0.84** |
| Random Forest | 0.88 | 0.20 | 0.75 |

**Outcome**: By performing **Threshold Optimization** (moving from the default 0.5 to 0.8285), we achieved a **Recall of 0.54** for the stroke class. This means the model successfully identifies over half of the actual stroke cases while maintaining high overall accuracy.

## 🚀 How to Run
1.  Clone the repository.
2.  Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3.  Open the notebook in Jupyter or Google Colab and run all cells.

## 🗂️ Files in this Repo
*   `stroke_prediction.ipynb`: The main project notebook containing EDA, Preprocessing, and Modeling.
*   `requirements.txt`: List of necessary Python libraries.
*   `healthcare-dataset-stroke-data.csv`: The dataset used for training.

## 🔮 Future Improvements
*   Experimenting with Gradient Boosting machines (XGBoost/LightGBM).
*   Feature engineering interaction terms between age and hypertension.
*   Deploying the model as a simple web app using Streamlit.






Stroke Prediction Analysis: Handling Imbalanced Healthcare Data
📌 Project Overview
This project aims to predict the likelihood of a patient having a stroke based on demographic and clinical features (e.g., age, hypertension, heart disease, BMI, and smoking status).

Predicting strokes is a critical healthcare challenge, further complicated by extreme class imbalance, as stroke cases typically represent a very small fraction (~5%) of the total population in the dataset.

🛠️ Methodology
To build a robust and reliable predictive system, the following pipeline was implemented:

Data Preprocessing:
Handled missing values in BMI using median imputation.
Feature scaling for numerical data and One-Hot Encoding for categorical features.
Automated the workflow using Scikit-Learn Pipeline and ColumnTransformer for reproducibility.
Imbalance Management:
Applied SMOTE (Synthetic Minority Over-sampling Technique) to balance the training set, allowing the models to learn patterns from the minority class effectively.
Model Evaluation:
Compared multiple algorithms: Logistic Regression and Random Forest.
Prioritized F1-Score and Recall over Accuracy due to the imbalanced nature of the target variable.
📈 Key Results
Model	Accuracy	F1-Score	AUC
Logistic Regression (Baseline)	0.63	0.24	0.84
Logistic Regression (Optimized)	0.91	0.37	0.84
Random Forest	0.88	0.20	0.75
Outcome: By performing Threshold Optimization (moving from the default 0.5 to 0.8285), we achieved a Recall of 0.54 for the stroke class. This means the model successfully identifies over half of the actual stroke cases while maintaining high overall accuracy.

🚀 How to Run
Clone the repository.
Install dependencies:
pip install -r requirements.txt
Open the notebook in Jupyter or Google Colab and run all cells.
🗂️ Files in this Repo
stroke_prediction.ipynb: The main project notebook containing EDA, Preprocessing, and Modeling.
requirements.txt: List of necessary Python libraries.
healthcare-dataset-stroke-data.csv: The dataset used for training.
🔮 Future Improvements
Experimenting with Gradient Boosting machines (XGBoost/LightGBM).
Feature engineering interaction terms between age and hypertension.
Deploying the model as a simple web app using Streamlit.
