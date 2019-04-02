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



  
### Classification
I will be testing to see if the decision tree or the SVC does a better job at classifying whether the type of wine is red or white using the wines features. 

The dataset was cleaned the same way as the linear regression notebook but this time the two types of wine were in the same data set so we could classify them.

#### Decision Tree
Initally I used the features alcohol and quality to see if it could be classified using those two features and it got these scores:

Confusion Matrix: 

  [93 1205
  
  58 3841]
  
- Accuracy is  0.7569751779873004

- Precision is  0.7249061994745626

- Sensitivity is  0.7569751779873004

- F1 is  0.6763696358184811

I changed the X features to alcohol, residual sugar, and volatile acidty. This time the model got much better scores: 

Confusion Matrix: 

  [1298   0
  
  13   3886]
  
- Accuracy is  0.9974985568597268

- Precision is  0.9975233614065029

- Sensitivity is  0.9974985568597268

- F1 is  0.99750270034275

#### SVC
Initally I used the same X features to predict the type as before, the alcohol, residual sugar, and volatile acidity. In the SVC the model scored a 91% whereas the decision tree scored a 99%. 

Confusion Matrix: 

  [974  324
  
  101  3798]
  
- Accuracy is  0.9182220511833751

- Precision is  0.9175633550841831

- Sensitivity is  0.9182220511833751

- F1 is  0.9155163519780091

So I decided to add another feature to see if it would do better. The second time I added chlorides to the list of features I used and it scored a 92% this time. When I tested it using the test set the accuarcy and F1 score went down 1% so it could be slightly overfitting. 

Confusion Matrix: 

  [994  304
  
  86   3813]
  
- Accuracy is  0.924956705791803

- Precision is  0.9247138539283412

- Sensitivity is  0.924956705791803

- F1 is  0.922537382531821


Here are some graphs to show kind of where the line between the different features would be to differentiate between the red and white wines.

![Comparing Alcohol and Acidity](https://github.com/44-599-machine-learning-S19/machine-learning-project-SierraK/blob/master/images/comparison1.PNG)

![Comparing Acidity and Sugar](https://github.com/44-599-machine-learning-S19/machine-learning-project-SierraK/blob/master/images/comparison2.PNG)

### Overall Results
The decision tree did a better job at classifying the type of wine with an accuracy and a F1 score of 99%. It used the features alcohol, residual sugar, and volatile acidity which makes sense because in the correlation heat maps those had the largest affects on the wine. 

The SVM did a little bit worse but still good with an accuracy and F1 score of 92% using the features alcohol, chlorides, volatile acidity, and residual sugar. There is a chance it is slighlty overfitting though because in the testing of the SVM it did slightly worse than the training set. 
  
  
  
  
  
  
  
  
  
  
  
  
  
  
