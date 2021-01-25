# Credit Card Default Prediction

```diff
Please note that this repository is incomplete and requires revision.
```

## Overview

This project aims to build a classification model that can predict whether or not a customer will default on their credit card. From the perspective of risk management, the result of predictive accuracy of the estimated probability of default will be valuable. After cleaning the data, handling class imbalance, feature engineering and tuning hyperparameters, the final Logisitic Regression model achieved an F1 score of 0.5418.

## Data Understanding

Link to research study [here](https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients).

This dataset contains information about customers' credit card default payments in Taiwan. The following 23 variables are the initial features included.

- X1: Amount of the given credit (NT dollar): it includes both the individual consumer credit and his/her family (supplementary) credit.
- X2: Gender
    - (1 = male; 2 = female).
- X3: Education 
    - (1 = graduate school; 2 = university; 3 = high school; 4 = others).
- X4: Marital status (1 = married; 2 = single; 3 = others).
- X5: Age (year).
- X6 - X11: History of past payment. We tracked the **past monthly payment dalay records** (from April to September, 2005) as follows:
    - X6 = the repayment status in September, 2005; 
    - X7 = the repayment status in August, 2005;
    - X8 = the repayment status in July, 2005;
    - X9 = the repayment status in June 2005;
    - X10 = the repayment status in May, 2005;
    - X11 = the repayment status in April, 2005
- The **measurement scale** for the repayment status is: 
    - -1 = pay duly
    - 1 = payment delay for one month
    - 2 = payment delay for two months; . . .;
    - 8 = payment delay for eight months; 
    - 9 = payment delay for nine months and above.
- X12-X17: Amount of bill statement (NT dollar).
    - X12 = amount of bill statement in September, 2005; 
    - X13 = amount of bill statement in August, 2005;
    - X14 = amount of bill statement in July, 2005;
    - X15 = amount of bill statement in June, 2005;
    - X16 = amount of bill statement in May, 2005;
    - X17 = amount of bill statement in April, 2005.
- X18-X23: Amount of previous payment (NT dollar)
    - X18 = amount paid in September, 2005
    - X19 = amount paid in August, 2005
    - X20 = amount paid in July, 2005
    - X21 = amount paid in June, 2005
    - X22 = amount paid in May, 2005
    - X23 = amount paid in April, 2005.
- Y: Whether or not they defaulted their payment
    - 1: Did default
    - 0: Did not default

NT is the abbreviation for New Taiwan dollar. 

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
