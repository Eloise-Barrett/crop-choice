# crop-choice
Using machine learning to identify which type of crop is best to plant based on the condition of the soil. The overall aim of this project is to identify which feature has the strongest predictive performance for classifying crop types. 

Project is from datacamp: https://app.datacamp.com/learn/projects/1772

## How it's made
Language: Python
Packages: pandas, sklearn, seaborn and matplotlib

The data was loaded and converted to a Dataframe using pandas where seaborn and matplotlib was then used to plot a graph to determine the distribution of the different types of crops in the dataset to determine if the dataset was balanced or not. After concluding the dataset was balanced, it was checked for null values, in which there were none. After this simple pre-processing, the data was seperated into features and a target before being further split into test and training data using sklearn. The features were then scaled using sklearn before a Logistic Regression model was created using sklearn with the 'multi_class' parameter set to ‘multinomial’ due to the problem being multiclass instead of binary. The model was then fit to only one feature at the time and then used to predict the crop type where the accuracy of the predictions was then recorded in a dictionary. Finally, the feature that produced predictions with the highest accuracy was identified as 'K' with an accuracy of 28.0 % (3 s.f.).

## Optimasations
The data was scaled in order to optimise the Logistic Regression models that are sensitive to scale and large numeric ranges. By scaling our data, we allowed the models to converge in fewer iterations and therefore sped up the process. Without the scaling, the models took over 1000 iterations to converge, whereas with scaling this was reduced to under 100.

## Future Direction
Future approaches for this project would focus on developing better models for determing the best crops to plant by increasing the accuracy of predictions. This could include looking at the feature interactions and builidng multi-feature models would likely increase the accuracy of the predictions for the crops. Another way to get better predictions for crops would be to explore different models that are more complex such as Random Forest or Neural Networks as well as combining these with cross-validation and hyperparamter tuning. 

## Lessons Learned
In this project, I learned the importance of properly preparing data, especially scaling features to help models converge efficiently. I also discovered that individual features can have varying levels of impact on prediction accuracy, emphasizing that some features are stronger predictors than others. However, testing each feature individually revealed that single features alone may not be very predictive, highlighting the need for combining multiple features. I also gained experience handling multiclass classification with logistic regression and interpreting model performance.
