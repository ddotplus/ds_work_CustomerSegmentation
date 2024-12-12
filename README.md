## Example Work: Customers Segmentation Using Credit Card Behaviors

### Purpose
- to develop a customer segmentation to define marketing strategy.

### Dataset
- usage behavior of \~9000 active credit card holders during 6 months.
- customers have 18 behavioral variables.
- data source: https://www.kaggle.com/datasets/arjunbhasin2013/ccdata/data
  - alternative source: https://github.com/andreduong-zz/credit-card-clustering/raw/refs/heads/master/CC%20GENERAL.csv
- variable details:

| Variable Name | Detail |
|:---|:---|
|CUST_ID | Identification of Credit Card holder (Categorical) |
| BALANCE | Balance amount left in their account to make purchases |
| BALANCE_FREQUENCY | How frequently the Balance is updated, score between 0 and 1 (1 = frequently updated, 0 = not frequently updated) |
| PURCHASES | Amount of purchases made from account |
| ONEOFF_PURCHASES | Maximum purchase amount done in one-go |
| INSTALLMENTS_PURCHASES | Amount of purchase done in installment |
| CASH_ADVANCE | Cash in advance given by the user |
| PURCHASES_FREQUENCY | How frequently the Purchases are being made, score between 0 and 1 (1 = frequently purchased, 0 = not frequently purchased) |
| ONEOFF_PURCHASES_FREQUENCY | How frequently Purchases are happening in one-go (1 = frequently purchased, 0 = not frequently purchased) |
| PURCHASES_INSTALLMENTS_FREQUENCY | How frequently purchases in installments are being done (1 = frequently done, 0 = not frequently done) |
| CASH_ADVANCE_FREQUENCY | How frequently the cash in advance being paid |
| CASH_ADVANCE_TRX | Number of Transactions made with "Cash in Advanced" |
| PURCHASES_TRX | Numbe of purchase transactions made |
| CREDIT_LIMIT | Limit of Credit Card for user |
| PAYMENTS | Amount of Payment done by user |
| MINIMUM_PAYMENTS | Minimum amount of payments made by user |
| PRC_FULL_PAYMENT | Percent of full payment paid by user |
| TENURE | Tenure of credit card service for user|

### Conclusion
- Method in brief:
  - observed *natural clusters* in variable correlations
  - selected related key variables for clustering: `BALANCE`, `PAYMENTS`, and `MINIMUM_PAYMENTS`
  - clustering model: *Bayesian Gaussian Mixture model*
  - clustering reliability test: *98+%* (for the case of five clusters)
- Resulting customer groups:
  - *conservative users* (small credit usuage)
  - *moderate users* (high-value users)
  - *immoderate users* (revolver)
  - *new users*
- Suggestions for marketing strategy
  - encourage *conservative users* to spend more and to use minimum payment and cash advance services
  - use loyality programs to retain *moderate users*, and encourage them to invite new users
  - encourage *new users* to use service often (to collect more usuage records)

#### MIT License
Copyright 2024 ddotplus@github
