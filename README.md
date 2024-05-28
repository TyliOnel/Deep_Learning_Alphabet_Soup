# Deep Learning Alphabet Soup Funding Success Predictor

## Background
The nonprofit foundation Alphabet Soup aims to select applicants for funding who have the best chance of success in their ventures. To assist in this endeavor, we will leverage machine learning and neural networks to create a binary classifier. This classifier will predict whether applicants will be successful if funded by Alphabet Soup.

## Dataset Information
We received a CSV file from Alphabet Soup’s business team containing data on more than 34,000 organizations that have received funding over the years. The dataset includes the following columns that capture metadata about each organization:

- EIN: Employer Identification Number (Identification column)
- NAME: Name of the organization (Identification column)
- APPLICATION_TYPE: Alphabet Soup application type
- AFFILIATION: Affiliated sector of industry
- CLASSIFICATION: Government organization classification
- USE_CASE: Use case for funding
- ORGANIZATION: Organization type
- STATUS: Active status
- INCOME_AMT: Income classification
- SPECIAL_CONSIDERATIONS: Special considerations for application
- ASK_AMT: Funding amount requested
- IS_SUCCESSFUL: Indicates whether the money was used effectively (binary target variable)

## Objective
The objective is to use the features in the provided dataset to build a model that can accurately predict the IS_SUCCESSFUL column. This binary classifier will help Alphabet Soup make informed decisions about which applicants to fund.

## Summary
Despite seven attempts, the model was unable to achieve a predictive accuracy higher than 73.7%. The only big difference I was able to see in the different models was when i dropped extra columns the model ran faster and was less accurate. Changing the the cutoff points and the different amount of layers had little to no affect on the accuracy result for the model. I recommend exploring alternative classification models to better predict the success of applicants funded by Alphabet Soup.
