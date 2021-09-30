# Neural_Network_Charity_Analysis

## Overview of Analysis
This project folder uses a Deep Neural Network model to analyze the effectiveness of donations to particular charitable organizations. The dataset contains metadata on these organizations, including their name, application type, income classification, asking amount, and finally the target variable, which is whether the donation was considered effective (binary variable). After preprocessing the data, I run the features through a Neural Network to determine if the model is able to accurately predict whether a donation would be considered effective. After trying a baseline Neural Network, I make adjustments to the model by dropping additional columns (“Classification”), adding different optimizers, adding additional hidden layers, and adding more neurons. Below I will summarize the results as well as provide a recommendation a different machine learning model to use instead of Neural Networks for this project.

## Results

*Data Preprocessing
  * What variable(s) are considered the target(s) for your model? The target variable is the IS_SUCCESSFUL column, which is a binary indicator of whether a particular organization is effective with the donations they receive. 
   * What variable(s) are considered to be the features for your model?
   
