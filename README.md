# Machine Learning Wine Quality Project

Developer: Sierra King

Data Set: https://www.kaggle.com/rajyellow46/wine-quality

## Initial Exploration
The data set contains information for both red and white wine. The information about the wine includes its physicochemical properties and the quality of the wine. Most of the data is numerical and it has some missing data. The missing data is filled using the mean of the column.

Predicting: Predict the quality of the wine using its properties. 

## Linear Regression
For the linear regression I have split the data set into the white and red wine data sets. The physicochemical properties should be different between the two types of wine so I felt that it was necessary to do so. 

Once the data sets were split into red and white wine they were then split into test and training sets with an 80/20 ratio. 

#### HeapMap showing Correlation for White Wine
![White Wine Heatmap](https://github.com/44-599-machine-learning-S19/machine-learning-project-SierraK/blob/master/images/lr_heatmap_white.png)


#### HeatMap showing Correlation for Red Wine
![Red Wine Heatmap](https://github.com/44-599-machine-learning-S19/machine-learning-project-SierraK/blob/master/images/lr_heatmap_red.png)

### Training
Training the model for the first time using the feature alcohol to predict the quality for both the red and white wine set. 

White Wine: 
- The R2 score is: 0.18294068827397758
- Mean Squared Error is:  0.6436278365855493

Red Wine: 
- The R2 score is: 0.22944655975826067
- Mean Squared Error is:  0.4997760282831427

Training the model for the second time for the white wine using the features alcohol, volatile acidity, residual sugar, and sulphates.
Training the model for the second time for the red wine using the features alcohol, volatile acidity, chlorides, and sulphates.

White Wine: 
- The R2 score is: 0.25546985764902086
- Mean Squared Error is:  0.5864939275727611

Red Wine: 
- The R2 score is: 0.34623470873378615
- Mean Squared Error is:  0.4240279825314856

### Testing
The same features used in the second training of the model were used for the testing.

White Wine: 
- The R2 score is: 0.2908622327476922
- Mean Squared Error is:  0.5450784051448285

Red Wine: 
- The R2 score is: 0.33885365578048865
- Mean Squared Error is:  0.43903603770100147
  
### Overall Results
When using the test set the scores were close but none of them were that high. Looking at the MSE the data does not appear to be overfitted because the numbers are very close. After doing some research perhaps using a decision tree or a random forest would be better to predict the quality of wine instead of using linear regression. 
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
