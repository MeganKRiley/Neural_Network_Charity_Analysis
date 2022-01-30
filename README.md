# Neural Network Charity Analysis

## Overview
The purpose of this analysis is to use the provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. 

## Data Preprocessing 
* The `IS_SUCCESSFUL` column is the variable that is considered the target for this model

* All of the variables except for the `IS_SUCCESSFUL` column and the columns we dropped are the targets for this model

* The `EIN` column and the `NAME` column are neither targets nor features, and therefore should be removed from the input data


## Compiling, Training, and Evaluating the Model 
* This neural network model includes two hidden layers.  The first layer has *80* neurons and the second layer has *30* neurons. The `relu` activation function is used in the first and second layer, while the `sigmoid` activation function is used for the output layer.

* I was unable to achieve the target model performance of *75%*.  The highest accuracy I achieved in my models was 65%.

* In attempt one I removed an additional feature - the `USE-CASE` column. My results stayed the same except my accuracy score decreased to *65%*.

<img width="419" alt="Attempt 1 Modification" src="https://user-images.githubusercontent.com/90050622/151721677-ce140ecb-05e3-40c8-bf55-5a6179db501a.png">
<img width="439" alt="Attempt 1 Results" src="https://user-images.githubusercontent.com/90050622/151721680-96d521c7-0f80-4e04-9c89-222f712abcaa.png">

* In attempt two I added both additional nuerons to the existing hidden layers, as well as the additional of more hidden layers.  This caused my accuracy score to decrease down to *53%*.

<img width="641" alt="Attempt 2 Modifications" src="https://user-images.githubusercontent.com/90050622/151721704-58490d6d-f6e7-473c-920e-e8df2e01c472.png">
<img width="440" alt="Attempt 2 Results" src="https://user-images.githubusercontent.com/90050622/151721711-f247e7dc-c4c5-44eb-8e0a-386e62e459e9.png">

* In my third attempt I changed the activation function of the output layer from `sigmoid` to `tanh`.  This modification decreased my accuracy score to *47%*.
<img width="633" alt="Attempt 3 Modifications" src="https://user-images.githubusercontent.com/90050622/151721752-e85c1c5b-cd27-4e9e-b7af-69bb2697383f.png">
<img width="440" alt="Attempt 3 Results" src="https://user-images.githubusercontent.com/90050622/151721757-37a2e4a9-2d16-4fef-aa61-6fc87ad31e1e.png">


## Summary
* In each attempt I made The accuracy score decreased. This was most likely caused by the model being overfitted. In a new attempt I would try removing more features in order to avoid the model from becoming overfitted again.  I think it would be beneficial to use the random forest classifier because it tends to have such a high accuracy.  
