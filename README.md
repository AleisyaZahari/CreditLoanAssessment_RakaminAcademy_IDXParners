Project based internship: Rakamin Academy x IDX Partner

---

# 📌 Credit Risk Prediction  

## 📂 Project Overview  
This project focuses on predicting **credit risk** for a lending company by analyzing historical loan data. The goal is to identify key factors influencing **bad loans** and develop a **machine learning classification model** to assess creditworthiness efficiently.  

## 🔍 Background  
A lending company faces challenges in streamlining the loan acquisition process for efficiency and quick handling of customer applications. As a **Data Science Intern at ID/X Partners**, the objective is to leverage **data analysis** and **predictive modeling** to enhance the loan application process.  

By harnessing data, **machine learning models** will be developed to accurately assess creditworthiness, speed up evaluations, and anticipate risks.  

## 💡 Business Understanding  
### ❓ Problem Statement  
- **11.6% of 466,000 customers** are classified as bad loans.  
- **Strategies are needed** to prevent bad loans by identifying influential factors.  

### 🎯 Goals & Objectives  
#### 📌 Goals  
- Identify **key factors** that influence bad loans.  

#### 🔹 Objectives  
- Perform **Exploratory Data Analysis (EDA)** 📊  
- Build a **machine learning classification model** 🤖  

## 🛠 Data Preprocessing  
### 🧼 Data Cleansing  
- 🗑 Remove columns with **>80% missing values** (except `last_pymnt_d`).  
- 🔄 Check and remove **duplicate records**.  
- 🚮 Drop **unnecessary columns**.  
- 🔍 Handle **correlated features**.  
- 🚫 Remove features with **no correlation** to the target.  

### ⚙️ Feature Engineering  
- 📅 Change data types for **date columns**.  
- 🔢 Create new features:  
  - `pymnt_time`: **Months** between `next_pymnt_d` & `last_pymnt_d`.  
  - `credit_duration_year`: **Years** between `earliest_cr_line` & `last_credit_pull_d`.  
- 🔄 Transform `term` from `"36 months"` & `"60 months"` ➝ **numeric (36, 60)**.  
- 🔬 Feature selection using:  
  - ✅ **Correlation analysis**  
  - 📈 **Biserial correlation**  
  - 📊 **Weight of Evidence (WOE) & Information Value (IV)**  
- 🏷 **Loan status classification**:  
  - ✅ "Good Loan": `Current`, `Fully Paid`, `In Grace Period`  
  - ❌ "Bad Loan": Any other status  
- 🔠 Feature encoding:  
  - 🔄 **One-hot encoding & label encoding**.  
  - 🔢 Encoding for **ordinal & nominal features**.  

## 🤖 Modeling and Evaluation  
### 🔬 Machine Learning Techniques  
- No assumption of **normal data distribution**.  
- ✅ **Robust to outliers**.  
- 📈 Model evaluation using **ROC-AUC** for risk discrimination capability.  

## 💼 Business Recommendations  
- **💰 Last Payment Amount**: Higher payments reduce bad loan risk.  
- **📉 Loan Amount**: Large loans + high interest = **higher risk**.  
- **📊 Total Payment**: Loans with payments **under $5000** are more likely to be **problematic**.  
- **⏳ Loan Duration**: **Longer repayment periods** = **higher risk**.  
- **📈 Interest Rate**: **Higher rates** correlate with **more bad loans**. Keeping rates lower can help reduce risks.  

## 🛠 Tech Stack  
- **Python** 🐍  
- **Pandas, NumPy** 📊  
- **Scikit-learn** 🤖  
- **Matplotlib, Seaborn** 📉  

## 🚀 Usage  
To run the analysis, open the **Jupyter Notebook (`.ipynb`)** and execute the cells sequentially. Ensure all dependencies and libraries are installed before running the scripts.  

---  
