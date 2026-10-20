# Student Dropout Analysis

Individual project for **WIH2001 Data Analytics**. This project applies the first three phases of the **CRISP-DM** methodology (Business Understanding, Data Understanding and Data Preparation) to a student dropout dataset.

## Dataset

- **Source:** [Kaggle – Student Dropout Prediction Dataset](https://www.kaggle.com/datasets/meharshanali/student-dropout-prediction-dataset)
- **Size:** 10,000 records and 19 attributes
- **Target variable:** `Dropout` (0 = retained, 1 = dropped out)

## Business Understanding

**Problem statement**
- High student dropout rates lead to lost academic potential and financial instability for both the university and the student.
- At-risk students are difficult to identify manually because financial, academic and personal factors are intertwined.

**Objectives**
- Identify the key factors that most strongly influence a student's decision to drop out.
- Explore the relationships between academic performance, stress, financial factors and student behaviour.

## Methodology

1. **Data Understanding** – summary statistics, target distribution, box plots, correlation heatmap and outlier detection (IQR method).
2. **Data Preparation**
   - Removed the irrelevant identifier column (`Student_ID`).
   - Imputed missing values with the median (numerical) and mode (categorical).
   - Capped `Family_Income` outliers at the IQR upper bound.
   - Binary and one-hot encoding of categorical variables.
   - Scaled numerical features with `StandardScaler`.

## Key Findings

- **Academic performance** is the strongest predictor: GPA and CGPA show a moderate negative correlation with dropout (r ≈ −0.45).
- **Stress index** is positively correlated with dropout (r ≈ 0.26).
- **Attendance rate** has a weak negative relationship with dropout (r ≈ −0.16).
- Dropouts are spread almost evenly across all five departments, suggesting a campus-wide issue.

## Repository Structure

```
├── IndividualAssignment23002459.ipynb   # Analysis notebook
├── student_dropout_dataset_v3.csv       # Dataset
├── requirements.txt                     # Required Python libraries
└── README.md
```

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook IndividualAssignment23002459.ipynb
```

## Tech Stack

Python · pandas · NumPy · Matplotlib · seaborn · scikit-learn · Jupyter Notebook

## Author

**Muhammad Adam Harith bin Mohd Zaki**
