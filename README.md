# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to implement the linear regression Model for Predicting the Marks Scored


## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## ALgorithm:

1.Start the program
2.Import the numpy,pandas,matplotlib
3.Read the dataset of student scores
4.Assign the columns hours to x and columns scores to y
5.From sklearn library select the model to train and test the dataset
6.Plot the training set and testing set in the graph using matplotlib library
7.Stop the program

## Program:
```
/*
Program to implement the linear regression for predicting the marks scored.
Developed by: Prakashraaj S
RegisterNumber: 21220040120 
*/
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
dataset=pd.read_csv("/content/sample_data/student_scores.csv")
dataset.head()
X=dataset.iloc[:,:-1].values
Y=dataset.iloc[:,1].values
print(X)
print(Y)
from sklearn.model_selection import train_test_split
X_train,X_test, Y_train,Y_test=train_test_split(X,Y,test_size=1/3,random_state=0)
from sklearn .linear_model import LinearRegression 
regressor=LinearRegression()
regressor.fit(X_train,Y_train)
LinearRegression()
Y_pred=regressor.predict(X_test)
plt.scatter(X_train,Y_train,color='yellow')
plt.plot(X_train,regressor.predict(X_train),color='green')
plt.title("h vs s(training set)")
plt.xlabel("Hours")
plt.ylabel("scores")
plt.show()
plt.scatter(X_test,Y_test,color='blue')
plt.plot(X_test,regressor.predict(X_test),color='green')
plt.title("h vs s(training set)")
plt.xlabel("Hours")
plt.ylabel("scores")
plt.show()
dataset.tail()
```


## Output:
![linear regression using predicting the arks scored](/output1.JPG)
![linear regression using predicting the arks scored](/output2.JPG)


## Result:
Thus the program to implement the linear regression using Predicting the marks scoed is written and verified using python programming.




