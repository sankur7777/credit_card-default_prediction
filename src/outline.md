# Outline
this outline serves as a checklist for the analysis notebook
the more specific the outline, the more helpful it is
- created from workflow exercise

## Data Comprehension
- See whether our target is continuous or categrical
- Figure out what 'row' represents
    - a person, an event, a geographic area
- comprehend all the features (what each feature represents

## Data Cleaning
Check for:
- NaN (missing) values
    - no missing values
- Correct datatypes
    - all floats and ints, no obj
- Outliers
- Duplicates
- Data integrity

## Data Preparation
- drop 'Unnamed: 0' column
    note: using the argument 'index_col=0` when loading in your dataframe makes sure this column doesnt appear
- replace whitespaces in column names

## EDA
- see if there are relationships between variables that can be used to create aditional variables
    - look at categories of variables and see if the distributions form together is specific ways
        - if so, we can bin them
    - look at scatterplots of continuous variables
        - if there are greoupings in those scatterplots, bin the categorical variables
        - if there are trends, we can create additional the variables that specify the relationship
            - if we see a exponential curve, we can create a new variable taking the log, etc.

## Modeling
- Step 1 is always train-test split
- Regression vs. Classification model
    - Because this is a categotical variable, we would use classification models
- Pick classification models to run
    - Logisitc Regression
    - KNN
- Run cross_validation process for baseline models for each potential model, to see how they do
    - run coss_val procudure on X_train and y_train
    - generate metrics for predictions against actual values, and avergage those metrics together
        - look at recall, because we want to select the models that do best at minimizing false negatives  
        
    - generate both training and testing metrics through cross-validataion to diagnose overfitting and underfitting

## Final analysis interpretation


## **2 takeaways of this exercise**
1. importance of using the outline
2. specifics of the cv train test workflow






