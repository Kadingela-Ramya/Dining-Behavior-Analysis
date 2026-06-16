Restaurant Tips — Exploratory Data Analysis
A data exploration project done as part of my internship. I picked the Tips dataset because it has a good mix of numeric and categorical features, which made it interesting to dig into tipping patterns across different groups.

What I Explored
The dataset has 244 restaurant transactions with info on total bill, tip amount, gender, smoker status, day, meal time, and party size. I wanted to understand what actually influences how much people tip — is it the bill size? The day? Who they are?

Dataset

Source: seaborn built-in (sns.load_dataset('tips'))
Rows: 244
Features: total_bill, tip, sex, smoker, day, time, size
Missing values: None


What I Did
Feature Engineering
Created a new column tip_pct — tip as a percentage of the total bill. Raw tip amount alone is misleading because a $5 tip on a $10 bill is very different from a $5 tip on a $50 bill.
Univariate Analysis
Looked at distributions of total bill, tip, and tip%. Most bills fall between $10–$25. Tips cluster around $2–$4. Saturday and Sunday had the most customers.
Bivariate Analysis

Total bill and tip have a strong positive correlation (~0.68) — bigger bills get bigger tips
Friday had the highest average tip percentage
Lunch customers actually tipped a slightly higher % than dinner customers
Smaller party sizes tipped more generously on a percentage basis

Multivariate Analysis
Used a heatmap to compare tip% across day and meal time combinations, and a FacetGrid to see how gender and bill size interact across different days.

Key Findings

Strongest tip predictor: total bill amount
Best tipping day: Friday
Large groups (5–6 people) tip the lowest % on average
Gender and smoker status have minimal impact on tip %
Most variability in tipping comes from individual behaviour, not demographics


How to Run

Open Restaurant_Tips_EDA.ipynb in Google Colab
Click Runtime → Run all
No installs needed — seaborn, pandas, matplotlib are all pre-installed


Tech Stack

Python 3.10+
pandas, numpy
seaborn, matplotlib
