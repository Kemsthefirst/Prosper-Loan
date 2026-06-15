# 💰 Prosper Loan Data Analysis

## 📌 Project Overview
This project explores a real-world lending dataset from Prosper — one of America's first peer-to-peer lending platforms. The goal was to clean the data, investigate borrower characteristics, and uncover patterns that could inform lending decisions and risk management strategies.

---

## 🗂️ Dataset
| Property | Detail |
|---|---|
| **Source** | kaggle |
| **Size** | 113,937 rows × 81 columns |
| **Domain** | Financial / Lending |
| **Tools Used** | Python, Pandas, Scipy, Matplotlib |

---

## 🧹 Data Cleaning Process

### 1. Column Reduction
Removed irrelevant columns that had no bearing on the analysis to streamline the dataset and reduce noise.

### 2. Data Type Conversion
Converted the `LoanOriginationDate` column from an **object** data type to **DateTime** format to enable accurate time-based analysis.

### 3. Missing Value Treatment
- **Numerical columns** → filled using the **mean** to preserve the overall distribution
- **Categorical columns** → filled using the **mode** (most frequent value) to maintain data integrity

### 4. Outlier Handling
Used **Winsorization** (`scipy.stats.mstats.winsorize`) to handle outliers in numerical columns. Winsorization replaces extreme values with less extreme boundary values rather than deleting them — preserving the row count while reducing the influence of anomalies.

### 5. Null Value Verification
Used `isnull()` to confirm no null values remained after treatment, then visualised the result to validate data completeness.

---

## ❓ Questions Investigated

### Univariate Analysis
- What is the distribution of borrower APRs in the dataset?
- How many borrowers are homeowners?
- What is the most common employment status among borrowers?
- What is the average monthly loan payment in the dataset?
- How many loans have been defaulted on?

### Bivariate Analysis
- Is there a relationship between a borrower's ProsperScore and their ProsperRating?
- Does employment status affect loan status?
- Is there a relationship between BorrowerAPR and LoanStatus?
- Does loan term impact a borrower's credit utilisation?
- Is there a connection between income range and the loan amount requested?

---

## 📊 Key Findings
- Borrower APR distribution revealed significant variation across credit tiers, with lower-rated borrowers facing considerably higher rates
- Employment status showed a clear correlation with loan status — employed borrowers had significantly better repayment outcomes
- Higher income ranges were associated with larger loan amounts requested, though credit score remained a stronger predictor of approval terms
- Loan term length had a measurable impact on credit utilisation, with longer terms correlating with higher utilisation rates

---

## 💡 Conclusion
The data exploration process revealed meaningful patterns linking borrower characteristics — including employment status, income range, credit score and APR — to loan outcomes. These insights could directly inform lending practices, helping platforms like Prosper improve risk assessment models and reduce default rates through more targeted loan management strategies.

---

## 🛠️ Tools & Libraries
- **Python** — core analysis
- **Pandas** — data manipulation and cleaning
- **Scipy** (`mstats.winsorize`) — outlier handling
- **Matplotlib** — data visualisation

---


