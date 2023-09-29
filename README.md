# deep-learning-challenge
Module 21 Challenge

## Overview
The goal of this project was to create an algorithm using machine learning and neural networks predictig whether applicants will be successful if funded by the fictional non-profit foundation, Alphabet Soup.

## Preprocessing
- drop non-beneficial columns
- find the number of data points for each unique value for each of the columns that had more than 10 unique values - APPLICATION_TYPE and CLASSIFICATION
- choose a cutoff point of 600 and 300, respectively, to bin rare categorical values together into a new value called "Other"
- use pd.get_dummies() to convert categorical data to numeric
- divide the data into a target array (IS_SUCCESSFUL) and features arrays
- apply the train_test_split to create a testing and a training dataset
- use StandardScaler to scale the training and testing sets
  
The resulting data included 44 features. The target variable (y) was IS_SUCCESSFUL. The data was split into training and test subsets.

## COMPILING, TRAINING, AND EVALUATING THE MODEL
The model was required to achieve a target predictive accuracy higher than 75%. I made three official attempts using machine learning and neural networks. They resulted in 72.5%, 72.7%, and 72.4% respectively.

Results from each model attempt are detailed below:

#1 - First attempt: 2 layers
72.5% of the model’s predicted values align with the dataset’s true values.

The hyperparameters used were:
  layer1 = 9 neurons : activation function = ‘relu’
  layer2 = 18 neurons : activation function = ‘relu’
  epochs = 100

#2 - Second attempt: added a hidden layer
72.7% of the model’s predicted values align with the dataset’s true values.

The hyperparameters used were:
  layer1 = 9 neurons : activation function = ‘relu’
  layer2 = 18 neurons : activation function = ‘relu’
  layer3 = 27 neurons : activation function = ‘relu’
  epochs = 100
  
#3 - Third attempt: 3 layers, changing the activation function for layers 1 and 2 
72.4% of the model’s predicted values align with the dataset’s true values.

The hyperparameters used were:
  layer1 = 9 neurons : activation function = ‘tanh’
  layer2 = 18 neurons : activation function = ‘sigmoid’
  layer3 = 27 neurons : activation function = ‘relu’
  epochs = 100

## Summary 
The attempts made did not exceed predictive accuracy higher than 72.7%. The second attempt had the highest, so I would build off of having a minimum of 3 hidden layers and increase the neurons in each layer while keeping the activation function the same.


## References
IRS. Tax Exempt Organization Search Bulk Data Downloads. https://www.irs.gov/Links to an external site.
