# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Ujjwal Anand

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
When I tried to submit my Predictions I came to know that we cannot submit results having negative values.
Thus to Submit my  predictions I had to Change all negative values of my predictions to 0.

### What was the top ranked model that performed?
Top ranked model is model with additional features.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
So I split datetime feature into new feature of year,month, day, hour. 
I found that temperature category was normally distributed where as workday and holidays had binary fields. Weather category had 3 input values. Humidity was left skewed and Windspeed was right skewed.

### How much better did your model preform after adding additional features and why do you think that is?
After adding more features my model improved by almost 66%.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
MOdel performance was bit worse then the model with only additional features. Better tunning will improve my model I think.

### If you were given more time with this dataset, where do you think you would spend more time?
I think working on hyperparameter will improve model performance.
Thus, i would have tried different hyperparameter combinations.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|default vals|default vals|default vals|1.8|
|add_features|default vals|default vals|default vals|0.690|
|hpo|NN epochs:[10],activation:['relu','softrelu',tanh'],layers[[100],[1000],[200,100],[300,200,100]]|GBM num_Boost_round: [100] no.of leaves [26,66]|default vals|0.4835|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

nd009t-c1-intro-to-ml-templates/project/nd009t-c1-intro-to-ml-project-starter/model_test_score.png

## Summary
I learned about autogluon and importance of EDA with this project and will try to use this learning in other projects as well.
