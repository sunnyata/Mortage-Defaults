# Mortage-Defaults
Mortgage Default Analysis &amp; Prediction


Introduction

The performance of mortgages is likely driven by a wide range of factors including borrower information, loan characteristics and macroeconomic effects. Loan or mortgage default is defined as the failure of the borrower to meets their obligation in repaying principal and interest on a loan. We would like to understand the most important drivers of defaults and predict which borrowers are likely to default at the time of mortgage origination (when the loan is written). 
Using publicly available data, I am building classification models to investigate the effect on loan performance of at least 12 variables. This credit analysis topic is central to the operations of banks and other lenders. It is also relevant to investors that purchase mortgage obligations (eg mortgage backed securities) from banks. Lenders (or investors) need to understand the risk they are taking when writing (or investing in) mortgages, with the key risk in lending being that of the loan not being repaid (i.e. default). 



Data Source 

Credit data is typically proprietary to banks and credit bureaus. One of the few sources of quality data is the Data Set Mortgage through Credit Risk Analytics, which can be accessed at: http://www.creditriskanalytics.net/datasets-private2.html .
Data Set Mortgage is a complex longitudinal (panel) dataset with 655,489 rows and 23 columns, covering 50,000 unique mortgage loans and their performance over time across 60 time periods. It is a randomized selection of mortgage-loan-level data collected from the portfolios underlying U.S. residential mortgage-backed securities (RMBS) securitization portfolios. Data on each unique mortgage includes: 

·	Information specific to the mortgage or property: variables on loan life (time since origination, time to maturity) loan balance, loan to property value (LTV) ratio, interest rate, real estate type (condominium or otherwise), development type (urban development or otherwise), home type (single family or otherwise), investor loan or otherwise 

·	Macroeconomic variables: gross domestic product (GDP) growth, unemployment rate, house price index 

·	Variable capturing the borrower’s past credit history: FICO credit score 

·	Variables capturing loan status: indicator variable for default, indicator variable for payoff (loan repaid or not), status (default, payoff and non-default/non-payoff) 
