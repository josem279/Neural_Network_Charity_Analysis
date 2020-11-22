# Neural_Network_Charity_Analysis

## Overview of Project

### Purpose

The purpose of this analysis was to create a binary clissifier capable of predicting the success of applicants that are funded by our company, Alphabet Soup. In order to create this classifier, we downloaded a large dataset, cleaned and preprocessed data, prepared and fitted neural networks, and then attempted to optimize our neural network by choosing to adjust one of the following: the number of neurons per hidden layer, the number of layers, the activation function for the hidden layers, or by adding additional epochs to the training regimen.

## Results

What variable(s) are considered the target(s) for your model?

- In the preprocessing section, the model initially considers the column "IS_SUCCESSFUL" within the "encoded_application_df" as the target.

What variable(s) are considered to be the features for your model?

- In the preprocessing section, the model considers all columns contained in the "encoded_application_df", except for the "IS_SUCCESSFUL" column as the features for the model. The following image shows how we designated targets and features in our model:

![image of targets/features](https://github.com/josem279/Neural_Network_Charity_Analysis/blob/main/Screenshots/FeaturesAndTargets.PNG)

What variable(s) are neither targets nor features, and should be removed from the input data?

- The columns "EIN" and "NAME" are considered neither targets or features, which is why they are removed from out DataFrame early in the preprocessing section of the challenge.
  
![image of removed non targets/features](https://github.com/josem279/Neural_Network_Charity_Analysis/blob/main/Screenshots/NonFeaturesOrTagets.PNG)


How many neurons, layers, and activation functions did you select for your neural network model, and why?

- I chose 2 layers of hidden_nodes for my model to get better deep learning and as I figured more layers may lead to overfitting. The first layer had 80 neurons and the second layer had 30 neurons following the rule of thumb that your first layer should contain roughly 2-3x the amount of inputs that your model contains (43 in this case). As for the activation functions, I chose to use the relu functions fas it simplifies the output. Finally, the Sigmoid function was chosen as the output activation function as it transforms the data to a range between 0 and 1 which makes it easier for the model to classify the whether a business is likely to be successful or not.

Were you able to achieve the target model performance?

- I was unable to achieve the 75% accuracy in my model even after I tried to optimize it.

What steps did you take to try and increase model performance?

- In order to try and achieve the target 75% performance I tried a couple of things. In my first attempt, I tried to increase the accuracy by increasing the number of neurons in the first and second layers but only got a 58% accuracy. In my second attempt, I tried to reduce the number of "noisy" inputs that I fed to my model, this led to a better accuracy of 62%. Finally, I tried to increase the number of values in each bin to reduce the number of unique values that the model evaluated. Again, my accuracy rating went up to 66% but failed to meet or exceed 75%.

![image of 1st optimized model output](https://github.com/josem279/Neural_Network_Charity_Analysis/blob/main/Screenshots/ResultsOpt1.PNG)

![image of 2nd optimized model output](https://github.com/josem279/Neural_Network_Charity_Analysis/blob/main/Screenshots/ResultsOpt2.PNG)

![image of 3rd optimized model output](https://github.com/josem279/Neural_Network_Charity_Analysis/blob/main/Screenshots/ResultsOpt3.PNG)

## Summary

Unfortunately my model output was not able to exceed 75% accuracy. However, the results revealed that there were things that could lead to better model performance. As a recommendation for better model performance we can take a better look at the data introduced in the preprocessing section. Here we can reduce noisy variables such as "STATUS" and exclude them as features. Moreover, it appears that adding more neurons also seems to improve model performance. Finally, it appears that grouping some of the more unique values/making larger bins that group unique values together also leads to better performance. 