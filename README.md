# Mortage-Defaults
Mortgage Default Analysis &amp; Prediction


## Introduction

The performance of mortgages is likely driven by a wide range of factors including borrower information, loan characteristics and macroeconomic effects. Loan or mortgage default is defined as the failure of the borrower to meets their obligation in repaying principal and interest on a loan. We would like to understand the most important drivers of defaults and predict which borrowers are likely to default at the time of mortgage origination (when the loan is written). 
Using publicly available data, I am building classification models to investigate the effect on loan performance of at least 12 variables. This credit analysis topic is central to the operations of banks and other lenders. It is also relevant to investors that purchase mortgage obligations (eg mortgage backed securities) from banks. Lenders (or investors) need to understand the risk they are taking when writing (or investing in) mortgages, with the key risk in lending being that of the loan not being repaid (i.e. default). 



## Data Source 

Credit data is typically proprietary to banks and credit bureaus. One of the few sources of quality data is the Data Set Mortgage through Credit Risk Analytics, which can be accessed at: http://www.creditriskanalytics.net/datasets-private2.html .
Data Set Mortgage is a complex longitudinal (panel) dataset with 655,489 rows and 23 columns, covering 50,000 unique mortgage loans and their performance over time across 60 time periods. It is a randomized selection of mortgage-loan-level data collected from the portfolios underlying U.S. residential mortgage-backed securities (RMBS) securitization portfolios. Data on each unique mortgage includes: 

- Information specific to the mortgage or property: variables on loan life (time since origination, time to maturity) loan balance, loan to property value (LTV) ratio, interest rate, real estate type (condominium or otherwise), development type (urban development or otherwise), home type (single family or otherwise), investor loan or otherwise 

- Macroeconomic variables: gross domestic product (GDP) growth, unemployment rate, house price index 

- Variable capturing the borrower’s past credit history: FICO credit score 

- Variables capturing loan status: indicator variable for default, indicator variable for payoff (loan repaid or not), status (default, payoff and non-default/non-payoff)

## Research questions
Primary Research Question: What variables can be used in predicting mortgage defaults and what classification models provide the best predictions?

Supporting Research Questions:

1.	How does the economic environment, or change in macro environment over time, impact mortgage performance?
2.	Can accurate default predictions be achieved without expectations of a future change in the macroeconomic environment?
3.	To what extent does additional loan structure and borrower information assist in identifying potential defaults? i.e. are a wide range of variables more useful than a small number of key variables?
   
## Modelling methodology

Data wrangling

Notwithstanding the panel data available, I do not seek to conduct an in depth time series analysis as my primary interest is in whether the loan ultimately defaults or not, and not its performance over time. As such, I will wrangle the dataset down to 50,000 observations.
I will nonetheless be able to draw information from other rows in the original >655,000 dataset through data transformations. I expect to create additional independent variables representing the change in variable value over time. For example, a change in interest rate over time from 5% to 8% (+3% change), will be more likely to see a default than a movement from 5% to 6% (+1% change) as the borrowers would have been comfortable servicing the loan initially but get into mortgage stress when rates rise significantly.
It would however need to be understood when using the model for prediction in the real world that such variables (like changes in interest rates) would need to be the expected future change in the variable given the change won’t yet have been experienced. That is, the data will be backward looking, whereas the goal is to achieve forward looking predictions.

Data mining & statistical learning methods

Given that a default is a binomial outcome making the dependent variable an indicator variable (the loan either performs and is repaid or else it defaults), classification modelling will be appropriate. I plan to to experiment with the following classification methods:
- Logistic regression
- Kth nearest neighbour (KNN)
- Linear discriminant analysis (LDA)
- Quadratic discriminant analysis (QDA)
- Naïve Bayes
- Support vector machine
- Decision trees, including through boosting or bagging
- Random forest


