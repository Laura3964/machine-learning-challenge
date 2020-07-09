# machine-learning-challenge
Three machine learning models were created to predict candidate exoplanets from the raw NASA Kepler dataset.
Data was preprocessed to remove null data and scaled accordingly with the MinMaxScaler function.
I chose all the features set to X, except for their corresponding error features.
A Decision Tree, Random Forest, and Logistic Regression models were trained and tested on the dataset.
The Decision Tree tested at approximately 85%
The Random Forest tested at approximately 90%
The Logistic Regression tested at approximately 80%
The best model was consistently the Random Forest model.
I utilized the Random Forest feature importance function and re-set X to those features with an importance > 0.05 and re-ran the Random Forest model. However, the result tested at less than 85%, so I re-set X to the orginal 20 features.
The Random Forest model's parameter for n_estimators was tuned using GridSearch where the larger n_estimator (1000) was chosen as the best parameter, versus 100.
Predictions were conducted on the tuned grid model with the following results:
 
 
 precision    recall  f1-score   support

     CANDIDATE       0.85      0.79      0.81       411
     CONFIRMED       0.84      0.86      0.85       484
FALSE POSITIVE       0.98      1.00      0.99       853

      accuracy                           0.91      1748
     macro avg       0.89      0.88      0.88      1748
  weighted avg       0.91      0.91      0.91      1748
