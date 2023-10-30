## Overview of the Analysis

### use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.
---

### Data
- The data was on loan risk status based on specific borrowers.

### Variables
- Features
  - Loan Size
  - Interest Rate
  - Borrower Income
  - Debt to Income
  - Number of Accounts
  - Derogatory Marks
  - Total Debt
- Target
  - Loan Status (Healthy or High-Risk)
---

### Estimators
- Trained a Logistic Regression model  after splitting the data into a training and testing set.
- Then used `RandomOverSampler` on the training data before refitting to a new Logistic Regression model so make the training data less bias.
---

### Results

#### Logistics Regression with out Random Over Sampler
- Accuracy Score: `95.2%`
- Precision: 
  - `100%` for Healthy Loans
  - `85%` for High Risk Loans
- Recall
  - `99%` for Healthy Loans
  - `91%` for High Risk Loans

#### Logistics Regression with Random Over Sampler
- Accuracy Score: `99.3%`
- Precision: 
  - `100%` for Healthy Loans
  - `84%` for High Risk Loans
- Recall
  - `99%` for Healthy Loans
  - `99%` for High Risk Loans

## Summary

#### Without random over sampling, there was a lot of bias for healthy loans due to the training data containing 75k healthy loans vs 2.5k High risk, that made the model better at predicting only Healthy loans. Using Random Over Sampler helped the recall of the new logistic regression model significantly increase!
