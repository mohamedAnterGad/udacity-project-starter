# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Mohamed Anter

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
we needed to make every score > 0 to submit my predicitons

### What was the top ranked model that performed?
weighted ensemble L2

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
we found that "season" and "weather" are int representation of category vaiables
I add "hour" feature representing the hour in the datetime

### How much better did your model preform after adding additional features and why do you think that is?
score in kaggle improved by 68%, I think this is because adding relevant features to the model helps it perform better.


## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
the score was 0.56 and became 0.48 it means increase by 14% in the kaggle score

### If you were given more time with this dataset, where do you think you would spend more time?
I would spend more time exploring the histograms of the featuers, making new features and cleaning the data(removing the outliers , normalizing the features...)

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|auto stack|hyperparameters|hyperparameters kwargs|score|
|--|--|--|--|--|
|initial|default value|default value|default value|1.79|
|add_features|default value|defautl value|default value|0.56|
|hpo|True|'multimodal'|'auto'|0.48|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![image.png](attachment:image.png)(img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![image-2.png](attachment:image-2.png)(img/model_test_score.png)

## Summary
we made the following :
 1- load the data
 2- EDA 
 3- base line model with autogluon with initial score of 1.79
 4- add a new feature (hour) and converted ('season' and'weather' to category) with score of 0.56
 5- perform hyper parameter tuning with score 0.48 
 6- future work: to make more feature engineering and make more new features
 

