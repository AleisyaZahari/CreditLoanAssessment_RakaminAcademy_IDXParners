Project based internship: Rakamin Academy x IDX Partner

# Credit Risk Prediction

## Project Overview
This project focuses on predicting credit risk for a lending company by analyzing historical loan data. The goal is to identify key factors influencing bad loans and develop a machine learning classification model to assess creditworthiness efficiently.

## Background
A lending company is facing challenges in streamlining the loan acquisition process to ensure efficiency and quick handling of customer applications. As a Data Science Intern at ID/X Partners, the objective is to leverage data analysis and modeling techniques to revolutionize the loan application process.

By harnessing data, predictive models will be developed to accurately assess creditworthiness, expediting the evaluation process and anticipating potential risks.

## Business Understanding

### Problem Statement
- 11.6% of 466,000 customers are classified as bad loans.
- Strategies are needed to prevent bad loans by identifying influential factors.

### Goals & Objectives
#### Goals
- Identify factors that influence bad loans.
#### Objectives
- Perform deep analytics (Exploratory Data Analysis - EDA).
- Build a machine learning classification model.

## Data Preprocessing

### Data Cleansing
- Remove columns with missing values exceeding 80% (except `last_pymnt_d`).
- Check and remove duplicate records.
- Remove unnecessary columns.
- Handle correlated features between independent variables.
- Handle features that do not have correlation with the target variable.

### Feature Engineering
- Change data type for date columns.
- Add new features derived from existing ones:
  - `pymnt_time`: Number of months between `next_pymnt_d` and `last_pymnt_d`.
  - `credit_duration_year`: Number of years between `earliest_cr_line` and `last_credit_pull_d`.
- Transform `term` feature from '36 months' and '60 months' to numerical values 36 and 60.
- Feature selection using:
  - Correlation analysis
  - Biserial correlation
  - Weight of Evidence (WOE) & Information Value (IV)
- Loan status classification:
  - "Good Loan": `Current`, `Fully Paid`, `In Grace Period`
  - "Bad Loan": Any other status
- Feature encoding:
  - One-hot encoding and label encoding for categorical variables.
  - Encoding for ordinal and nominal features.

## Modeling and Evaluation

### Machine Learning Techniques
- No assumption of normal data distribution.
- Robust to outliers.
- Model evaluation using ROC-AUC to measure model discrimination capability.

## Business Recommendations
- **Last Payment Amount**: Increasing customer payment amounts reduces the probability of high-risk loans.
- **Loan Amount**: Higher loan amounts correlate with higher interest rates, increasing risk.
- **Total Payment**: Loans with payments in the range of 0 to 5000 are more likely to be problematic.
- **Loan Duration**: Longer repayment durations increase the chance of high-risk loans.
- **Interest Rate**: Higher interest rates correlate with higher bad loan rates; consider maintaining lower rates.

## File Structure

### Table of Contents in Jupyter Notebook (`.ipynb`)
1. **Download Data**
2. **Import Library**
3. **Read Dataset**
4. **Data Description**
5. **Data Understanding**
6. **Data Cleansing**
   - Handling Missing Values
   - Check Duplicates
   - Delete Unnecessary Columns
7. **Feature Engineering**
   - Change Data Type for Date
   - Add New Features
   - Change Feature Term
   - Check Target Value (`loan_status`)
8. **Exploratory Data Analysis**
   - Correlation Analysis
     - Numerical Features
     - Biserial Correlation
     - Categorical Features
   - Check Correlation to Target
   - Check Correlation Between Features
   - Univariate Analysis (Numerical & Categorical)
   - Bivariate Analysis
9. **Feature Engineering**
   - Weight of Evidence (WOE) & Information Value (IV)
   - Feature Engineering on:
     - `loan_amnt`
     - `int_rate`
     - `annual_inc`
     - `dti`
     - `delinq_2yrs`
     - `inq_last_6mths`
     - `open_acc`
     - `pub_rec`
     - `revol_util`
     - `total_acc`
     - `out_prncp`
     - `total_pymnt`

## Usage
To run the analysis, open the Jupyter Notebook (`.ipynb`) and execute the cells sequentially. Ensure that all necessary dependencies and libraries are installed before running the scripts.

---
This README provides an overview of the project, methodology, and key insights derived from the data analysis and model development. The detailed implementation can be found in the Jupyter Notebook file (`.ipynb`).

