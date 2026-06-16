Dining Behavior Analysis
I did this as part of my data science internship. The dataset is about restaurant tips — 244 transactions with info like bill amount, tip, gender, day, time, and party size. I wanted to figure out what actually makes people tip more or less. Turns out it's not always what you'd expect.

Why This Dataset
I picked the Tips dataset because it has a good mix of numbers and categories. It's small enough to understand completely but interesting enough to find real patterns in. Also I wanted to practice working with both numeric and categorical data in the same project.

Dataset Details

Source: seaborn built-in dataset (sns.load_dataset('tips'))
244 rows, 7 columns
Columns: total_bill, tip, sex, smoker, day, time, size
No missing values


What I Did
Feature Engineering
The first thing I noticed is that raw tip amount doesn't tell the full story. A $3 tip on a $10 bill is very different from a $3 tip on a $50 bill. So I created a new column called tip_pct which is just tip divided by total_bill multiplied by 100. This became my main metric throughout the project.
Univariate Analysis
Looked at how each column is distributed on its own before comparing anything. Most bills were between $10 and $25. Tips clustered around $2 to $4. Saturday had the most customers by far.
Bivariate Analysis
This is where things got interesting. I compared tip_pct against every other column one by one.

Total bill and tip amount have a strong positive correlation of around 0.68 which means bigger bills do get bigger tips but not proportionally
Friday had the highest average tip percentage even though it had fewer customers
Lunch customers tipped a higher percentage than dinner customers which surprised me
Smaller tables tipped more generously percentage-wise than large groups

Multivariate Analysis
Combined multiple variables at once. Used a heatmap to see how tip percentage changed across different day and time combinations. Used a FacetGrid to split by day and color by gender to see if patterns held across the week.
Statistical Summaries
Calculated mean, median, and standard deviation of tip_pct for every group — gender, day, smoker status, time. This helped me separate actual patterns from things that just looked different visually.

Key Findings

Biggest driver of tip amount is total bill size — that correlation is real
Friday lunch is the best tipping scenario in this dataset
Groups of 1 or 2 people tip around 3 to 4 percent more than groups of 5 or 6
Gender and smoker status had very little effect on tip percentage
Most of the variation in tipping comes down to individual behaviour, not demographics


Visualizations Made

Histograms for total bill, tip, and tip percentage
Bar charts for day, time, gender, smoker counts
Scatter plot with trend line for total bill vs tip
Boxplots for tip percentage by day and time
Violin plots for tip percentage by gender and smoker status
Bar chart for average tip percentage by party size
Heatmap for day vs time combination
FacetGrid split by day and colored by gender
Correlation matrix for all numeric columns


How to Run

Open Restaurant_Tips_EDA.ipynb in Google Colab
Runtime → Run all
Everything runs without installing anything extra


Libraries Used

pandas
numpy
matplotlib
seaborn



