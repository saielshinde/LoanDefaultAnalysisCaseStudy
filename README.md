# Loan Default Analysis

## Overview
This project analyzes a dataset of loan applicants to identify factors influencing loan defaults. Using Exploratory Data Analysis (EDA), it aims to uncover patterns and insights that can help reduce credit loss by identifying high-risk applicants.

## Objectives
1. Identify key variables affecting loan default.
2. Understand the relationships between borrower attributes and default likelihood.
3. Provide actionable insights for risk assessment and decision-making.

## Dataset
- **Source**: Loan applicant data
- **Key Features**:
  - `loan_status`: Loan repayment status (e.g., Fully Paid, Charged-off)
  - `annual_inc`: Annual income of applicants
  - `grade`: Loan grade (A to G)
  - `dti`: Debt-to-income ratio
- **Target Variable**: `loan_status` (Charged-off indicates default)

## Workflow
### 1. Data Preprocessing
- **Missing Values**:
  - Dropped columns with more than 40% missing values.
  - Numeric columns filled with median values.
  - Non-numeric columns filled with "Unknown".
- Saved the cleaned dataset as `cleaned_loan_data.csv`.

### 2. Univariate Analysis
- Visualized the distribution of individual features:
  - Loan status (`loan_status`)
  - Annual income (`annual_inc`)

### 3. Bivariate Analysis
- Analyzed relationships between features and `loan_status`:
  - Loan grade (`grade`) vs. Loan status
  - Debt-to-income ratio (`dti`) vs. Loan status

### 4. Correlation Analysis
- Generated a correlation matrix for numeric features to identify significant relationships.

## Key Findings
1. **Loan Grade**:
   - Lower grades (D, E) show higher default rates.
   - Higher grades (A, B) are associated with lower risk.
2. **Annual Income**:
   - Borrowers with annual income <$50,000 are more likely to default.
   - Mild negative correlation between income and default probability.
3. **Debt-to-Income Ratio (DTI)**:
   - Higher DTI correlates with increased default likelihood.
   - Borrowers with DTI > 40% are at higher risk.
4. **Correlation Analysis**:
   - Weak correlations observed between numeric variables, suggesting low multicollinearity.

## Outputs
- **Cleaned Dataset**: `cleaned_loan_data.csv`
- **Visualizations**: Key plots generated for univariate, bivariate, and correlation analyses.

## Conclusion
The analysis identifies critical factors like loan grade, income, and DTI as strong indicators of loan default. These insights can guide lending decisions and reduce financial risk.

---

*Developed using Python and Google Colab.*
