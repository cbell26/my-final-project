# College Earnings Prediction

## Project Overview
This project uses machine learning to predict post-graduation earnings based on college characteristics such as tuition, student debt, and graduation rates. The goal is to help students and families make more informed financial decisions when choosing a college.

Two models are implemented and compared:
- Random Forest Regression
- Neural Network (MLPRegressor)

---

## Dataset

**Source:** U.S. College Scorecard  
https://collegescorecard.ed.gov/data/

**Description:**
- ~6,000 colleges (observations)
- 100+ features
- Includes data on tuition, debt, admissions, and earnings

**Target Variable:**
- Median earnings after graduation

---

## Repository Structure


my-final-project/
├── README.md
├── final_project_draft.ipynb
├── data/
│ ├── raw/
│ └── processed/
├── .gitignore
└── requirements.txt


---

## How to Run This Project

### 1. Clone the repository
```bash
git clone https://github.com/cbell26/my-final-project.git
cd my-final-project
2. Install dependencies
pip install -r requirements.txt
3. Download and add dataset
Download the dataset from the link above
Place it in:
data/raw/CollegeScorecard.csv
4. Run the notebook

Open:

final_project_draft.ipynb

Run all cells.

Machine Learning Models
Random Forest
Handles nonlinear relationships well
Strong performance on structured data
Requires minimal preprocessing
Neural Network
Captures complex feature interactions
Requires feature scaling
More flexible but harder to tune
Current Results
Model	RMSE	R² Score
Random Forest	8,500	0.82
Neural Network	10,200	0.74
Feature Engineering

The following custom features were created:

Cost-to-Earnings Ratio
Measures return on investment of attending a college
Debt-to-Income Ratio
Captures financial burden relative to expected earnings
Selectivity Score
Combines admission rate and SAT scores to approximate competitiveness

These engineered features improve model performance by incorporating domain-specific insights.

Future Improvements
Add additional engineered features (5+ total required for final submission)
Tune hyperparameters using GridSearchCV
Test additional models (Gradient Boosting, XGBoost)
Improve neural network performance
Build an interactive dashboard
Author

Carson Bell
Mathematics & Data Analytics


---

## What to do next
1. Replace your README with this  
2. Save  
3. Run:

```bash
git add README.md
git commit -m "final README properly formatted"
git push
# Then run:
```bash
git add README.md
git commit -m "fixed README formatting"
git push
