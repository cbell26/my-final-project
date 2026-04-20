# College Admissions Prediction Using Machine Learning

## Project Overview

This project applies machine learning techniques to predict **college admission rates** using institutional characteristics such as tuition, academic performance, and student demographics.

The objective is to:

* Identify key factors influencing college selectivity
* Build predictive models to estimate admission rates
* Provide actionable insights for students, institutions, and policymakers

Two machine learning models are developed, optimized, and compared:

* **Linear Regression (baseline model)**
* **Random Forest Regressor (optimized model)**

---

## Project Evolution (Important)

This project was **originally designed to predict post-graduation earnings**. However, during data exploration, it became clear that earnings-related variables contained **extensive missing values**, making them unusable for modeling.

After attempting multiple cleaning strategies, the dataset resulted in **zero usable observations**, preventing meaningful analysis.

### Pivot Decision

To address this issue and ensure a valid project:

* The target variable was changed to **admission rate (`ADM_RATE`)**
* A new modeling approach was developed using more complete features

This pivot reflects a realistic data science workflow:

> Adapting to data limitations while still delivering valuable, reliable insights.

---

## Dataset

**Source:** U.S. College Scorecard
https://collegescorecard.ed.gov/data/

### Description:

* ~6,000 colleges (observations)
* 100+ variables
* Covers admissions, cost, student demographics, and outcomes

### Final Target Variable:

* **Admission Rate (`ADM_RATE`)**

---

## Repository Structure

```
my-final-project/
│
├── final_project.ipynb        # Final submission notebook
├── final_project_draft.ipynb  # Draft version (iteration reference)
├── README.md
├── data/
│   └── raw/
│       └── college_data.csv
├── .gitignore
└── requirements.txt
```

---

## How to Run This Project

### 1. Clone the repository

```bash
git clone https://github.com/cbell26/my-final-project.git
cd my-final-project
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Add dataset

Download the dataset and place it here:

```
data/raw/college_data.csv
```

### 4. Run the notebook

Open:

```
final_project.ipynb
```

Run all cells from top to bottom.

---

## Feature Engineering

To improve model performance, several engineered features were created:

* **COST_PER_STUDENT**
  Tuition adjusted for student population size

* **SELECTIVITY_SCORE**
  Combines SAT scores and admission rate to approximate competitiveness

* **SAT_AVG**
  Proxy for academic rigor

* **TUITIONFEE_OUT**
  Indicator of institutional positioning

* **UGDS (Undergraduate Size)**
  Captures scale of institution

* **PCTPELL**
  Proxy for socioeconomic diversity

These features help capture deeper patterns beyond raw data.

---

## Machine Learning Models

### 1. Linear Regression

* Baseline model
* Fast and interpretable
* Assumes linear relationships

### 2. Random Forest (Optimized)

* Handles nonlinear relationships
* More robust to noise
* Tuned using:

  * Number of trees
  * Maximum depth

---

## Final Results

| Model             | MSE          | R² Score     |
| ----------------- | ------------ | ------------ |
| Linear Regression | (your value) | (your value) |
| Random Forest     | (your value) | (your value) |

### Key Findings:

* Random Forest outperformed Linear Regression
* SAT scores and tuition are strong predictors
* Engineered features improved predictive accuracy

---

## Visualizations Included

* Feature distributions
* Correlation heatmap
* Predicted vs Actual scatter plot
* Feature importance chart

These visualizations help interpret model behavior and performance.

---

## Ethical Considerations

This model may reflect **systemic inequalities in education**:

* SAT scores and income-related variables may introduce bias
* Schools serving lower-income populations could be disadvantaged
* Predictions may reinforce existing inequities if misused

### Mitigation Strategies:

* Avoid fully automated decision-making
* Monitor model bias across groups
* Use predictions as **support tools**, not final decisions

---

## Business Recommendations

### Actionable Insights:

* Institutions can adjust recruitment strategies based on key predictors
* Tuition and academic metrics strongly influence selectivity
* Schools can benchmark competitiveness using model outputs

### Deployment Strategy:

* Use as a **decision-support tool**
* Retrain annually with updated data
* Monitor for performance drift and bias

### Limitations:

* Does not capture qualitative admissions factors (essays, extracurriculars)
* Correlation ≠ causation
* Dependent on historical data quality

---

## Final Recommendation

The **Random Forest model** is recommended for deployment due to:

* Higher predictive accuracy
* Ability to capture complex relationships
* Better overall performance on test data

---

## Author

**Carson Bell**
Mathematics & Data Analytics
Aspiring Data Scientist

git add README.md
git commit -m "final README with project pivot and full analysis"
git push
