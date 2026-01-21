# Sales-Data-Preprocessing

## Table of Contents 

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Preprocessing](#data-preprocessing)
- [Data Analysis](#data-analysis)
- [Results](#results)
- [References](#references)

### Project Overview 
Performed comprehensive data auditing and cleaning on a sales dataset by identifying missing values, handling duplicates and generating statistical summaries to ensure data integrity for downstream analytical modeling.

### Data Sources 
A raw "Sales.csv" dataset from Kaggle containing transactional records, product categories and customer metadata used for auditing and preprocessing workflows.

### Tools
- Python
- Pandas
- Google Colab

### Data Preprocessing 
Executed automated data cleaning by auditing missing values, calculating null percentages and identifying duplicate records to ensure a high-fidelity dataset for analysis.

### Data Analysis
```Python
import pandas as pd
import matplotlib.pyplot as plt
df= pd.read_csv('/content/Sales.csv')
print(df)
df.shape
df.info()
df.describe().round()
df.isnull().sum()
df.isnull().sum()/len(df)*100
df[df.duplicated()].shape
df[df.duplicated()]
```

### Results 
Successfully validated data quality by identifying the exact percentage of missing values and isolating duplicate entries, resulting in a structured, error-free dataset ready for business intelligence reporting.

### References 
1. Dataset Source: Kaggle- Sales
   - [https://www.kaggle.com/datasets/sales]
2. Tool Documentation: Pandas
   - [https://pandas.pydata.org/docs/]
3. Analysis Methodology: Inspired by Data Preprocessing for best practices for content streaming platforms.
