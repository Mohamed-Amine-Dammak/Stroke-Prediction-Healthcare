
**Healthcare / Predictive Analytics Project**  
**Imen Abdelkader & Mohamed Amine Dammak** – 2024 

Predicting stroke risk using clinical and lifestyle features (5,110 patients). Strong focus on **high Recall** (catch as many true strokes as possible) – critical for medical applications.

![Python](https://img.shields.io/badge/python-3670A0?style=flat&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=flat&logo=pandas&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-239120?style=flat&logo=plotly&logoColor=white)

## Goal
Build a reliable model to predict stroke probability and identify the most important risk factors.

## Dataset – healthcare-dataset-stroke-data.csv
- 12 features: age, hypertension, heart disease, glucose level, BMI, smoking status, etc.
- Target: `stroke` (1 = had a stroke) → **highly imbalanced** (only ~5% positive cases)

## Key Steps Implemented
- Comprehensive EDA & interactive Plotly visualizations
- Missing BMI handling + outlier detection (Isolation Forest)
- Categorical encoding & scaling
- Class imbalance handling: **SMOTE** & **ADASYN**
- 8 classification models with GridSearchCV
- Evaluation focused on **Recall first**, then F1-Score and Accuracy

## Best Performing Models (Recall-oriented)
| Rank | Model                     | Recall | F1-Score | Accuracy |
|------|---------------------------|--------|----------|----------|
| 1    | Gradient Boosting + SMOTE | **0.92**| 0.78     | 0.88     |
| 2    | Random Forest + ADASYN    | 0.90   | 0.76     | 0.87     |
| 3    | Logistic Regression       | 0.88   | 0.74     | 0.85     |

## Repository Contents
.
├── healthcare-dataset-stroke-data.csv      # Original dataset
├── Stroke Prediction Code.ipynb            # Full notebook (EDA → Modeling → Evaluation)
└── README.md                               # This file
text## How to Run
```bash
# Clone the repository
git clone https://github.com/Mohamed-Amine-Dammak/Stroke-Prediction-Healthcare 

# Navigate into the project folder
cd Stroke-Prediction-Healthcare

# Install required Python packages
pip install pandas numpy scikit-learn imblearn plotly seaborn matplotlib

# Launch the Jupyter Notebook
jupyter notebook "Stroke Prediction Code.ipynb"

# To stop Jupyter Notebook later
Ctrl + C
y  # confirm shutdown

# To exit Git Bash
exit

