Dining Behavior Analysis — Exploratory Data Analysis
Overview
This project performs Exploratory Data Analysis on a restaurant tips dataset to uncover patterns in customer tipping behaviour. It helped me understand how to explore data systematically and present findings in a meaningful way.
Objective
To analyze what factors influence how much customers tip at restaurants and identify key patterns across gender, day, time, and party size.
Tech Stack

Python
Pandas, NumPy
Matplotlib, Seaborn
Google Colab

Approach

Loaded the Tips dataset from seaborn built-in library
Checked for missing values, data types, and class distributions
Created a new feature tip_pct (tip as percentage of total bill) for better comparison
Performed univariate analysis on all numeric and categorical columns
Performed bivariate analysis comparing tip_pct against every other column
Used multivariate analysis with heatmaps and FacetGrid
Calculated group-wise statistical summaries — mean, median, standard deviation

Results

Total bill size has the strongest correlation with tip amount (r = 0.68)
Friday had the highest average tip percentage across the week
Smaller party sizes (1 to 2 people) tipped around 3 to 4 percent more than large groups
Lunch customers tipped a higher percentage than dinner customers
Gender and smoker status had very little impact on tipping behaviour

Project Files

Restaurant_Tips_EDA.ipynb

How to Run
1. Open Restaurant_Tips_EDA.ipynb in Google Colab
2. Click Runtime → Run all
3. No installations needed — all libraries are pre-installed in Colab



