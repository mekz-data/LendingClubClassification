# LendingClubClassification
 Classifying Defaults on Lending Club Loans

Data Science project to determine features that are most important to determine defaults on personal loans.

Takeaways: Best features for predicting default before a loan is ever issued are: borrowers with a high number of months since oldest revolving account opened, lower loan amounts & payments, a low number of total accounts, higher annual incomes, and a high number of months since the most recent installment accounts were opened.

File Listing:
Column Descriptions.xlsx - descriptions of the 100+ columns in the dataset.

Final Report Doc.pdf - Written report of my process including more detailed discussion of our problem and the conclusions reached. Features many snipped images from the jupyter notebooks.

Jupyter Notebooks:
0 – Initial Data Cut: This is a really short notebook where I cut the data from 11 years of data down to
three.

1 – Data Cleaning: shows all manner of data cleaning and pruning of features.

2 – Exploratory Data Analysis: EDA is performed along with one hot encoding and further pruning of features to prepare the data for Machine Learning.

3 – Initial ML Testing: testing out logistic regression, Random Forest, and Gradient Boosting algorithms on our data including experimenting with upsampling and downsampling.

4 – Hyperparameter Optimization and Final Analysis: attempts optimizing our Gradient Boosting algorithm and ends with an exploration of the model's feature importances to determine best predictors of loan defaults.
