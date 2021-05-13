# Credit_Card_Fraud_Detection

Source: https://www.kaggle.com/mlg-ulb/creditcardfraud

The dataset contains transactions made by credit cards in September 2013 by European cardholders.
This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.

It contains only numerical input variables which are the result of a PCA transformation. Unfortunately, due to confidentiality issues, we cannot provide the original features and more background information about the data. Features V1, V2, … V28 are the principal components obtained with PCA, the only features which have not been transformed with PCA are 'Time' and 'Amount'. Feature 'Time' contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature 'Amount' is the transaction Amount, this feature can be used for example-dependant cost-sensitive learning. Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 otherwise.

Given the class imbalance ratio, we recommend measuring the accuracy using the Area Under the Precision-Recall Curve (AUPRC). Confusion matrix accuracy is not meaningful for unbalanced classification.

Steps for Execution:

1. Extrcated the data and checked the information adn the description for the data and if there are any null values in it.
2. Checked the correlation for the data.
3. As the data has some negative and positive values, so the we can conlude the data has already been scaled and its mentioned in the descriptionas well.
4. Since its a huge dataset we can't do all our computations on it so taking a sample from the dataset of 25% which has been picked randomly.
5. Now we can perform the Exploratory Data Analysis on this sample.
6. Checked the number of values are for the proper transaction and how many are for the fraud ones.
7. Split the dataset into training and testing data depending on the X and y features.
8. Trained a simple Logistic Regressor model for classification using the train and test data.
9. Evaluated the performance with the Classification Report and the results are as mentioned below.

Classification Report:

              precision    recall  f1-score   support

           0       1.00      1.00      1.00     21324
           1       0.67      0.59      0.63        37

    accuracy                           1.00     21361
    
   macro avg       0.83      0.80      0.81     21361
   
weighted avg       1.00      1.00      1.00     21361
