# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries and load the employee salary dataset using Pandas.

2.Preprocess the dataset by separating input features and target salary values, and convert categorical data into numerical format.

3.Create and train the Decision Tree Regressor model using the dataset.

4.Predict the employee salary using the trained model and display the performance metrics and decision tree visualization.



## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Priyadharshini V
RegisterNumber: 212225230219



import pandas as pd

data = pd.read_csv("Salary.csv")

print(data.head())

print(data.info())

print(data.isnull().sum())

from sklearn.preprocessing import LabelEncoder

le = LabelEncoder()
data["Position"] = le.fit_transform(data["Position"])

print(data.head())

x = data[["Position", "Level"]]
y = data["Salary"]

from sklearn.model_selection import train_test_split

x_train, x_test, y_train, y_test = train_test_split(
    x, y, test_size=0.2, random_state=2
)

from sklearn.tree import DecisionTreeRegressor

dt = DecisionTreeRegressor(random_state=2)

dt.fit(x_train, y_train)

y_pred = dt.predict(x_test)

from sklearn import metrics

mse = metrics.mean_squared_error(y_test, y_pred)
print("Mean Squared Error:", mse)

r2 = metrics.r2_score(y_test, y_pred)
print("R2 Score:", r2)

prediction = dt.predict([[5, 6]])

print("Predicted Salary:", prediction[0])
 
*/
```

## Output:

<img width="647" height="649" alt="Screenshot 2026-05-19 114111" src="https://github.com/user-attachments/assets/69a3f8df-b2c2-4e3e-a072-c966e3794cdb" />


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
