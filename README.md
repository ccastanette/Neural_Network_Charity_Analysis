# Neural_Network_Charity_Analysis

## Overview
  
  The purpose of this analysis is to train a machine learning model that will return an accuracy of greater than 75%
  
## Technology:

  1. Jupyter Notebooks
  2. sklearn
  3. pandas
  4. tensorflow
  
## Results:

  Preprocessing
  
    - The variable that is considered the target is IS_SUCCESSFUL

    - All other variables that were not dropped were features of the model:
      1. APPLICATION_TYPE
      2. AFFILIATION
      3. CLASSIFICATION
      4. USE_CASE
      5. ORGANIZATION
      6. INCOME_AMT
      7. SPECIAL_CONSIDERATIONS
      
    - The variables that are unimportant and were dropped are:
      1. EIN
      2. NAME

## Compiling, Training, and Evaluating the Model

### Optimization Attempt 1

On the first attemp the number of neurons on each layer was increased to 100 just to see if simply increasing the number of neurons would make a significant difference in the results.

    Total number of hidden layers:2
    Number of neurons: 
      layer 1:100 
      layer 2:100
    activiation functions: 
      layer 1: relu 
      layer 2: relu

![attemp1model](https://github.com/ccastanette/Neural_Network_Charity_Analysis/blob/main/pics/attempt1model.png)

### Attemp 1 Results:
![attempt1reults](https://github.com/ccastanette/Neural_Network_Charity_Analysis/blob/main/pics/attempt1result.png)


### Optimization Attempt 2

On the second attempt both of the activation functions were switched to tahn to see if that function would be more successfull in training the model.

    Total number of hidden layers:2
    Number of neurons: 
      layer 1:100 
      layer 2:100
    activiation functions: 
      layer 1: tahn 
      layer 2: tahn

![attemp1model](https://github.com/ccastanette/Neural_Network_Charity_Analysis/blob/main/pics/attempt2model.png)

### Attemp 2 Results:
![attempt1reults](https://github.com/ccastanette/Neural_Network_Charity_Analysis/blob/main/pics/attempt2result.png)

### Optimization Attempt 3

On the third attempt another hidden layer was added as well as switching the activation functions to be a mix of relu & tahn.

    Total number of hidden layers:2
    Number of neurons: 
      layer 1:100 
      layer 2:100
      layer 3:100
    activiation functions: 
      layer 1: relu 
      layer 2: tahn
      layer 3: relu

![attemp1model](https://github.com/ccastanette/Neural_Network_Charity_Analysis/blob/main/pics/attempt3model.png)

### Attemp 1 Results:
![attempt1reults](https://github.com/ccastanette/Neural_Network_Charity_Analysis/blob/main/pics/attempt3result.png)

## Summary

None of the attempts were able to get an accuracy of greater than 75%. I would suggest dropping the special considerations feature and classification features they might be adding too much niose to the model. I would also recommend trying both a support vector machine and a random forest model to see if those would be more successful.
