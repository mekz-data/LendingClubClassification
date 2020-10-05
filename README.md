# Predicting Defaults on Personal Loans

<img src="https://github.com/Huntsworth7/LendingClubClassification/blob/master/images/lending_club_logo.JPG">

Building a model to predict defaults on loans from Lendingclub, a peer-to-peer lending company.

This was my first ever Data Science project. At least the first one that contains all the typical steps of cleaning, EDA, visualization, and model building.
I wanted a topic that I had familiarity with. I worked in the mortgage industry for several years and spent a lot of time analyzing similar data
to pre-qualify clients for homes so I was really in my element here.   

## Project Overview:
- Model accurately classified 96% of good loans and 76% of defaulted loans. 
- Original dataset was from [kaggle](https://www.kaggle.com/wordsforthewise/lending-club) and was cut down to 3 years.
- Large dataset even after cutting: 1.3 million rows by 151 columns.
- With so many features, extensive EDA was performed.
- Experimented with Logistic Regression, Gradient Boosting, and Random Forest algorithms with upsampling and downsampling.
- Hyperparameter Optimization using Gaussian Processes.
- Analysis of feature importances to determine best predictors of loan defaults.

## File List
**Column Descriptions.xlsx:** Descriptions for the 100+ columns in the dataset.<br>
**Final Report Doc.pdf:** Written report of my process including more detailed discussion of our problem and the conclusions reached. It contains many visualizations from the jupyter notebooks.<br>

**<ins>Jupyter Notebooks:</ins>**
- **0 – Initial Data Cut:** Short notebook where I cut the data from 11 years of data to the years 2015-2017.
- **1 – Data Cleaning:** All manner of data cleaning and pruning of features.
- **2 – Exploratory Data Analysis:** Extensive EDA is performed along with one hot encoding and further pruning of features to prepare the data for Machine Learning.
- **3 – Initial ML Testing:** Testing out multiple algorithms including Logistic Regression, Random Forest, and Gradient Boosting. Also experimented with upsampling and downsampling.
- **4 – Hyperparameter Optimization and Final Analysis:** Attempted optimization of our Gradient Boosting algorithm and ends with an exploration of the model's feature importances to determine best predictors of loan defaults.

## Code and Resources Used
**Python Version:** 3.7<br>
**Packages used:** pandas, numpy, matplotlib, scikit-learn, LightGBM, Seaborn, Imblearn, and scikit-optimize.<br>
**Article:** [Hyperparameter Tuning with Bayesian Optimization](https://medium.com/@vincent.kr18/hyper-parameter-tuning-using-bayesian-optimisation-code-b50e0e8abe20)


## Features
The dataset has far too many features to go over all of them but the most important ones include:
- **Interest Rate:** the interest rate on the loan.
- **Fico Score & Most Recent Fico Score:** Fico score at loan approval and most recent fico score.
- **Total Accounts:** Total accounts on borrower's credit.
- **Annual Income:** Annual income earned by the borrower
- **Employment Length:** How long the borrower has been employed at their current company.
- **Loan Amount:** The amount financed.  
- **Debt-to-income:** the monthly debts that the borrower is obligated on divided by monthly income.   

## Data Cleaning
- Removed many columns. Review the jupyter notebook for my reasoning.
- Converted employment length column from string to integer.
- Dropped some rows that had a few missing values.
- Filled some missing values with the median.
- Filled some missing values with -999 to indicate that the event in question never occurred.

## EDA
With so many features, exploratory Data Analysis makes up quite a bit of this project and I would encourage you to look at my notebook if you're at all curious at what all was done.

## Model Building
I worked with Logistic Regression, Gradient Boosting, and Random Forest algorithms. As this was a highly imbalanced dataset (only 15% of loan were defaulted), I also experimenting with upsampling to balance this out. 


## Model Performance
Here's the ROC curve for all three classifiers. Gradient Boosting outperforms Random Forest by the slimmest of margins: <br><br>
<img src="https://github.com/Huntsworth7/LendingClubClassification/blob/master/images/roc_curve.JPG" width="540">

Hyperparameter Optimization was performed but did not yield any noticeable improvements.

## Takeaways
According to our model, the most important features for predicting a good loan are:
- borrowers with a high number of months since oldest revolving account opened
- lower loan amounts & payments
- a low number of total accounts
- higher annual incomes
- a high number of months since the most recent installment accounts were opened.

This project was a great learning experience. Looking at it again while updating this Readme, I see plenty of improvements or augmentations that I would make if I were working on it today. That being said, I am going to keep it as it is to act as my Data Science time capsule.
