# Sales-Data-Preprocessing

## Table of Contents 

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Preprocessing](#data-preprocessing)
- [Data Analysis](#data-analysis)
- [Data Visualization](#data-visualization)
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
### Data Visualization
```Python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

df = pd.read_csv('Sales.csv')
plt.figure(figsize=(10, 5))
sns.boxplot(x=df['Customer_Age'], color='skyblue')
plt.title('Distribution of Customer Age (Outlier Detection)', fontsize=15)
plt.xlabel('Age')
plt.grid(axis='x', linestyle='--', alpha=0.7)
plt.show()

import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

df = pd.read_csv('Sales.csv')
country_revenue = df.groupby('Country')['Revenue'].sum().sort_values(ascending=False).reset_index()
plt.figure(figsize=(12, 6))
sns.barplot(data=country_revenue, x='Country', y='Revenue', palette='viridis')
plt.title('Total Revenue by Country', fontsize=15)
plt.xlabel('Country', fontsize=12)
plt.ylabel('Total Revenue (USD)', fontsize=12)
plt.xticks(rotation=45) 
plt.tight_layout()
plt.show()
```
### Results 
Successfully validated data quality by identifying the exact percentage of missing values and isolating duplicate entries, resulting in a structured, error-free dataset ready for business intelligence reporting.

### References 
1. Dataset Source: Kaggle- Sales
   - [https://www.kaggle.com/datasets/sales]
2. Tool Documentation: Pandas
   - [https://pandas.pydata.org/docs/]
3. Analysis Methodology: Inspired by Data Preprocessing for best practices for content streaming platforms.
