# Task 3 - Data Cleaning

## Internship
Oasis Infobyte - Data Analytics Internship

## Objective

The objective of this task is to clean and prepare a student dataset by identifying and handling missing values, duplicate records, inconsistent categorical values, potential outliers, and data type issues.

## Dataset

- **Dataset:** Student Dataset for Data Cleaning, EDA and Predictive Modeling
- **Source:** Kaggle
- **Dataset Link:** https://www.kaggle.com/datasets/walekhwatlphilip/intro-to-data-cleaning-eda-and-machine-learning
- **Raw File:** `bi.csv`
- **Rows:** 77
- **Columns:** 11

## Tools Used

- Python
- Pandas
- NumPy
- Jupyter Notebook

## Data Cleaning Process

### 1. Initial Data Quality Check

The dataset was inspected to understand its structure and identify data quality issues.

The following checks were performed:

- Dataset shape
- Data types
- Missing values
- Duplicate records
- Descriptive statistics
- Categorical value consistency

Initial findings:

- 77 rows and 11 columns
- 2 missing values in the `Python` column
- 0 duplicate rows
- The `Python` column had a `float64` data type because of the missing values

### 2. Handling Missing Values

Two missing values were identified in the `Python` column.

The missing values were replaced using the median Python score.

**Median Python score:** 81

Median imputation was used because the median is less affected by extreme values than the mean.

### 3. Duplicate Records

The dataset was checked for duplicate rows.

- Duplicate rows found: **0**
- No records were removed due to duplication.

### 4. Standardizing Inconsistent Values

Several categorical values had inconsistent formatting or naming. These were standardized to improve consistency.

Examples include:

- `M`, `male` → `Male`
- `F`, `female` → `Female`
- `norway`, `Norge` → `Norway`
- `Rsa` → `South Africa`
- `UK` → `United Kingdom`
- `Somali` → `Somalia`
- `BI-Residence`, `BIResidence`, `BI_Residence` → `BI Residence`
- `HighSchool` → `High School`
- Education spelling and case variations were standardized.

### 5. Outlier Detection

The Interquartile Range (IQR) method was used to identify potential numerical outliers.

A total of **10 potential outlier rows** were identified during the screening process.

The identified observations were retained because their values were considered plausible and there was no clear evidence that they were data-entry errors.

Therefore, the outliers were treated as valid observations rather than being automatically removed.

### 6. Data Type Correction

After handling the missing values, the `Python` column was converted from:

`float64` → `int64`

This was done because the column contains whole-number Python scores after missing-value treatment.

## Before vs After

| Metric | Before | After |
|---|---:|---:|
| Rows | 77 | 77 |
| Columns | 11 | 11 |
| Missing Values | 2 | 0 |
| Duplicate Rows | 0 | 0 |
| Python Data Type | float64 | int64 |

## Final Dataset

After cleaning:

- **Rows:** 77
- **Columns:** 11
- **Missing values:** 0
- **Duplicate rows:** 0
- **Numerical columns:** 5
- **Categorical/Text columns:** 6

The cleaned dataset is included in this folder as:

`Gousiya_Noorain_Task3_cleaned.csv`

## Files

- `Gousiya_Noorain_Task3_Data_Cleaning.ipynb` — Complete data cleaning workflow
- `Gousiya_Noorain_Task3_cleaned.csv` — Cleaned dataset

## Conclusion

The student dataset was successfully cleaned while preserving valid observations. Missing values were handled using median imputation, duplicate records were checked, inconsistent categorical values were standardized, potential outliers were evaluated using the IQR method, and data types were corrected.

The final dataset contains **77 rows and 11 columns**, with **0 missing values and 0 duplicate records**. The cleaned dataset is ready for further analysis and predictive modeling.
