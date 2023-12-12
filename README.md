# Home Equity Loan Default Risk Analysis

## Project Overview
This project analyses the risk of default on home equity loans using Logistic Regression and Random Forest models. The goal is to predict the likelihood of loan default based on various borrower characteristics.

## Data Description
The dataset features 5,960 home equity loans with attributes such as loan amount, mortgage due, property value, job category, and credit history. Key variables include:
- `LOAN`
- `MORTDUE`
- `VALUE`
- `YOJ`
- `DEROG`
- `DELINQ`
- `CLAGE`
- `NINQ`
- `CLNO`
- `JOB`

## Methodology
### 1. Data Preprocessing
- **Exploratory Data Analysis**: Histograms, box plots, and correlation analysis.
- **Handling Missing Values**: Implemented strategies like deletion and imputation.
- **Outlier Detection**: Treated using capping methods.
- **WoE Transformation**: Applied for Logistic Regression.

### 2. Model Development
- **Logistic Regression**: Used WoE-transformed data, focusing on high IV variables.
- **Random Forest**: Applied on raw data for comparison.

### 3. Performance Evaluation
Evaluated using metrics such as Accuracy, Precision, Recall, F1 Score, ROC-AUC, and MCC. Random Forest outperformed Logistic Regression across all metrics.

### 4. Feature Importance
Highlighted features for each model:
- Random Forest: `BAD`, `LOAN`, `MORTDUE`, `VALUE`, `YOJ`, `DEROG`, `DELINQ`, `CLAGE`, `NINQ`, `CLNO`.
- Logistic Regression: Scorecard developed based on IV analysis.

## Key Findings
- WoE transformation significantly improved Logistic Regression's performance.
- Random Forest's superior performance attributed to its handling of non-linear relationships and complex interactions.

## Conclusion
The comparison between Logistic Regression and Random Forest provides valuable insights into credit risk analysis, highlighting the importance of model selection based on the specific requirements of the task.

## Usage
To replicate the analysis:
1. Clone the repository.
2. Open the Jupyter Notebook (`<HomeEquityLoan_DefaultRiskAnalysis>.ipynb`).
3. Download the HMEQ dataset.
4. Execute the cells to view the analysis and results.
