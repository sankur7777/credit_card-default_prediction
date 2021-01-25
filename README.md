# Credit Card Default Prediction

```diff
Please note that this repository is incomplete and requires revision.
```

![banner](./visualizations/banner.jpg)

## Overview

This project aims to build a classification model that can predict whether or not a customer will default on their credit card. From the perspective of risk management, the result of predictive accuracy of the estimated probability of default will be valuable. After cleaning the data, handling class imbalance, feature engineering and tuning hyperparameters, the final Logisitic Regression model achieved an F1 score of 0.5418.

## Data Understanding

Link to research study [here](https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients).

This [dataset](https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients) contains information about customers' credit card default payments in Taiwan.

### Cleaned Dataset

| Column Name | Description |
|-|-|
| max_credit_given | Amount of the given credit (NT dollar). it includes both the individual consumer credit and his/her family (supplementary) credit. |
| gender | 1 = male; 2 = female |
| education | 1 = graduate school; 2 = university; 3 = high school; 4 = others |
| marital_status | 1 = married; 2 = single; 3 = others |
| age |  |
| pay_status_sept | Amount of montly payment delay record, broken down from April to September 2006. |
| pay_status_aug |  |
| pay_status_july |  |
| pay_status_june |  |
| pay_status_may |  |
| pay_status_april |  |
| bill_sept | Amount of bill statement (NT dollar) |
| bill_aug |  |
| bill_july |  |
| bill_june |  |
| bill_may |  |
| bill_april |  |
| payment_sep | Amount of previous payment (NT dollar) |
| payment_aug |  |
| payments_jul |  |
| payment_jun |  |
| payment_may |  |
| payment_april |  |
| Y | Whether or not they defaulted their payment. 1 = did default; 0 = did not default |

NT is the abbreviation for New Taiwan dollar. 

The **measurement scale** for the repayment status is: 
    - -1 = pay duly
    - 1 = payment delay for one month
    - 2 = payment delay for two months [...]
    - 8 = payment delay for eight months
    - 9 = payment delay for nine months and above

## Methods

This is a binary classification problem where the target variable is default payment (Yes = 1, No = 0).

After cleaning the data, handling class imbalance and feature engineering, several baseline models were fit to the training data. Baselines included K Nearest Neigbors, Logistic Regression and Decision Trees. Each model iteration's hyperparameters were tuned with GridSearchCV. Predictions were evaluated using the **F1 Score.

## Final Model Analysis
The final Logisitic Regression model achieved an F1 score of 0.5418.


## Repository Contents
```bash
.
├── notebooks                          # contains modeling notebooks
├── pickle                             # contains models and scalers
├── visualizations                     # contains graphs and images
├── src                                # source folder
│   └── training_data.csv              # raw dataset
├── README.md                          # public-facing preview
└── final_notebook.ipynb               # final version of EDA, feature engineering and modeling process


```

## For More Information
- See the [full project overview](https://github.com/sidneykung/cc_default_prediction/blob/master/final_notebook.ipynb) in the `final_notebook.ipynb` Jupyter Notebook.
- For additional information or suggestions, contact Sidney Kung at [sidneyjkung@gmail.com](mailto:sidneyjkung@gmail.com)

**Let's connect!**

- [LinkedIn](https://www.linkedin.com/in/sidneykung/)

- [Twitter](https://twitter.com/sidney_k98)
