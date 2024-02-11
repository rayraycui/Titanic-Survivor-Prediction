# Titanic-Survivor-Prediction
 A project that uses the Titanic Survivor dataset in kaggle to predict whether a given passenger survived or not given the age, class, sex, cabin etc. 

STEPS:

1. I first imported the necessary libraries for this project such as numpy pandas and sklearn.

2.  I then read in the csv file from the training and testing dataset (so i didnt need to split the entire data) and set my features and label accordingly.

3.  Since i want to use a KNN model, I would need to convert all the categorical values in my data to numerical values. I would also need to deal with all of the missing values in my data. I deal with numerical missing values by using an imputer to replace all of the missing values in numerical columns to the mean of the rest of the values. I deal with categorical missing values by also using an imputer and setting the missing value to the most frequent categorical value in each column. I convert the categorical values to numerical values by using onehot encoding and dropping the categorical features with a very high number of unique classes.

4.  I set K ot 6, indicating that I am considering only the 6 closest neighbors to any given datapoint. I then initialize the model and fit the model to my training data. (Note, this is a competition and therefore, in the dataset for testing, there is no 'survived' category, and therefore, i cannot obtain results but i can print predictions.

5.  Predictions (0=no, 1=yes): [0 0 0 0 0 0 1 1 0 1 0 0 0 0 0 1 0 0 0 0 0 0 1 1 1 0 1 0 0 0 1 1 0 0 1 0 0
 0 0 1 0 0 0 0 1 0 0 0 1 0 1 0 1 1 0 0 0 0 0 1 0 1 0 1 1 0 0 0 0 1 0 0 0 0
 0 0 0 0 0 0 1 1 1 0 0 0 1 0 1 1 0 0 1 0 0 0 1 0 0 0 1 0 0 0 0 0 0 0 0 0 1
 1 0 0 1 0 0 1 1 1 0 0 1 0 0 0 0 1 0 0 0 0 0 0 0 0 0 0 0 0 0 1 1 1 0 0 0 0
 0 0 1 0 0 0 0 0 0 0 0 0 1 1 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 1 0 1 1 0 1
 0 0 0 0 0 1 0 1 0 0 0 1 0 0 0 0 1 1 0 0 0 0 0 1 0 0 0 0 0 0 0 1 1 1 0 0 0
 0 0 0 0 0 1 0 0 1 1 0 0 1 0 1 0 0 0 0 0 1 0 0 1 0 0 1 0 1 0 1 0 0 0 0 0 0
 0 0 0 0 1 0 0 0 0 0 0 1 0 1 0 0 1 0 0 0 0 0 1 1 1 1 0 0 1 0 0 0 1 0 1 0 0
 1 0 0 0 0 0 0 0 1 0 1 1 0 0 0 0 0 0 1 0 1 0 0 1 0 0 0 1 1 0 0 1 1 0 0 0 0
 0 0 0 1 0 1 0 0 0 0 1 0 1 0 0 0 0 0 0 0 1 1 1 1 0 0 1 0 0 0 0 1 0 0 0 0 0
 0 1 0 0 1 1 0 0 0 0 0 0 0 0 0 1 0 0 0 0 1 0 0 0 1 1 0 1 0 0 1 0 1 0 0 0 0
 1 1 1 1 1 0 0 1 0 0 0]
