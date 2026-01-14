# HR Employee Retention & Satisfaction Analysis

An exploratory and inferential analysis of employee data to identify patterns in retention and investigate the statistical significance of factors like workload and satisfaction levels.

## Overview

This project focuses on HR analytics to understand employee behavior and attrition. By analyzing a dataset of 14,999 records, the study examines how variables such as satisfaction scores, evaluation results, number of projects, and average monthly hours correlate with an employee's decision to stay or leave the organization.

## Dataset

- **Source:** HR "people.csv" dataset, containing organizational and performance metrics.
- **Key columns:**
  - `satisfactoryLevel`: Employee satisfaction score (0 to 1).
  - `lastEvaluation`: Score from the most recent performance review.
  - `numberOfProjects`: Number of projects assigned to the employee.
  - `avgMonthlyHours`: Average hours worked per month.
  - `timeSpent.company`: Years of experience in the company.
  - `left`: Target variable (1 if employee left, 0 otherwise).
  - `dept`: Department name (e.g., Sales, IT, HR).
  - `salary`: Salary level (Low, Medium, High).

## Objectives

- Perform comprehensive **Data Cleaning** and preprocessing, including deduplication and label encoding.
- Conduct **Exploratory Data Analysis (EDA)** to visualize employee distributions across departments and salary tiers.
- Use **Hypothesis Testing** to validate assumptions about employee workload and satisfaction.
- Identify critical drivers of employee attrition (e.g., correlations between low satisfaction and high workloads).

## Methods and Analysis

The analysis follows a rigorous data science workflow:

- **Data Cleaning and Preprocessing**
  - Identifies and removes **3,008 duplicate records** to ensure data integrity.
  - Renames columns (e.g., `timeSpent.company` to `Time Spent in company`) for better readability.
  - Utilizes **Label Encoding** to convert categorical variables like `dept` and `salary` into numerical formats for analysis.

- **Statistical Analysis (Inferential Stats)**
  - **T-Tests:** Used to determine if there is a significant difference in the `avgMonthlyHours` between employees with different levels of experience (e.g., 2–5 years vs. 6–10 years).
  - **Decision Criteria:** Employs a significance level of $\alpha = 0.05$. In specific tests, the analysis failed to reject the null hypothesis, suggesting that average monthly hours did not differ significantly between certain experience cohorts.

- **Visualization (EDA)**
  - Frequency distributions of satisfaction levels.
  - Comparisons of performance vs. attrition rates.

## Tech Stack

- **Language:** Python 3
- **Libraries:**
  - `pandas` and `numpy`: Data manipulation and cleaning.
  - `seaborn` and `matplotlib`: Visualizing trends and distributions.
  - `scipy.stats`: Core statistical testing (T-tests).
  - `sklearn.preprocessing`: Label encoding for categorical data.
- **Environment:** Jupyter / Google Colab

## How to Run

1. Clone this repository:
   ```bash
   git clone [https://github.com/](https://github.com/)<your-username>/hr-retention-analysis.git
   cd hr-retention-analysis

2. *Create and activate a virtual environment (optional but recommended):*
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate

3. *Install dependencies:*
   pip install pandas numpy seaborn matplotlib scipy scikit-learn

4. *Open the notebook:*
   jupyter notebook 12_HR_Analytics_casestudy.ipynb
