# Neural_Network_Charity_Analysis

## Overview of Analysis
This project folder uses a Deep Neural Network model to analyze the effectiveness of donations to particular charitable organizations. The dataset contains metadata on these organizations, including their name, application type, income classification, asking amount, and finally the target variable, which is whether the donation was considered effective (binary variable). After preprocessing the data, I run the features through a Neural Network to determine if the model is able to accurately predict whether a donation would be considered effective. After trying a baseline Neural Network, I make adjustments to the model by dropping additional columns (“Classification”), adding different optimizers, adding additional hidden layers, and adding more neurons. Below I will summarize the results as well as provide a recommendation a different machine learning model to use instead of Neural Networks for this project.

## Results

* Data Preprocessing
  * What variable(s) are considered the target(s) for your model? The target variable is the IS_SUCCESSFUL column, which is a binary indicator of whether a particular organization is effective with the donations they receive. 
   * What variable(s) are considered to be the features for your model? All other non-target variables, except for the ones I dropped. Since I dropped the EIN, NAME, and ORGANIZATION variable, this would be: APPLICATION_TYPE, AFFILIATION,	CLASSIFICATION,	USE_CASE,	STATUS,	INCOME_AMT,	SPECIAL_CONSIDERATIONS,	and ASK_AMT.
   * What variable(s) are neither targets nor features, and should be removed from the input data? I removed EIN, NAME, and the ORGANIZATION variables since they provide no beneift to the model. 
* Compiling, Training, and Evaluating the Model
   * How many neurons, layers, and activation functions did you select for your neural network model, and why? In my optimized version, I used 12 neurons on hidden layer 1 and hidden layer 2, and 16 neurson on the hidden layer 3. I increased the number of neurson from 6 on hidden layer 1 and 2 in the baseline model to see if this would increase performance. I also added a third layer to the Neural Network to see if this would produce a better outcome. Finally, I adjusted the activation functions on the hidden layer to Sigmoid and the closing layer to RElu to see if this improved the outcome, but it did not. 
   * Were you able to achieve the target model performance? I was not. The best I was able to get to was 72%, which was with the baseline model. Below are the results.

[Baseline Model Results](https://github.com/SethBoswell/Neural_Network_Charity_Analysis/blob/main/Images/baseline%20model%20results.png)

   * What steps did you take to try and increase model performance? I dropped the 'ORGANIZATION' variable because it did not provide additional information to help train the model. I then increased the number of neurons, added another hidden layer, and changed the activation functions. Below is the setup and the results, which weren't as good as the baseline model.

[Optimized Model Results](https://github.com/SethBoswell/Neural_Network_Charity_Analysis/blob/main/Images/optimized%20model%20results.png)

[Optimized Model Performance](https://github.com/SethBoswell/Neural_Network_Charity_Analysis/blob/main/Images/optimized%20model%20performance.png)

### Summary
In sum, my baseline model with 2 hidden layers, 6 neurons on each, and Relu activation functions on the hidden layers and Sigmoid on the closing layer was the most successful. If I had to guess, I think the Relu activation functions is probably better on the hidden layers than Sigmoid. 72% accuracy is not terrible, but I think other models would do better in this case.
Specifically, I would recomend using a logistic regression model over this Neural Network. The outcome variable is a binary indicator that would be perfect for logistic regression, which is simpler than a Deep Learning model. Combined with PCA analysis, my guess is the logistic regression model would be a better predictor of whether a charitable organization would be effective with their donations compared to the Neural Network presented here. 

   
