# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the libraries and read the data frame using pandas.
2. Calculate the null values present in the dataset and apply label encoder.
3. Determine test and training data set and apply decison tree regression in dataset.
4. Calculate Mean square error,data prediction and r2.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: S.PAVAN
RegisterNumber: 25001333


import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()

data.info

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position","Level"]]
y=data[["Salary"]]

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse

r2=metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])



*/
```

## Output:
DATA HEAD:
<img width="477" height="326" alt="image" src="https://github.com/user-attachments/assets/d0c4ccd0-1670-4b5f-a815-8e4875fc2b5b" />

DATA INFO:
<img width="741" height="295" alt="image" src="https://github.com/user-attachments/assets/9a2d2af0-8691-4fb5-b9f9-9d45b80c0fff" />

isnull() issum():
<img width="245" height="109" alt="image" src="https://github.com/user-attachments/assets/02da259a-8dc4-4bee-8f93-96c0386596d3" />

Data Head for salary:
<img width="399" height="292" alt="image" src="https://github.com/user-attachments/assets/e45bd92e-1bd8-4ae8-975e-486ecf2ccaea" />

Mean Squared Error :
<img width="296" height="48" alt="image" src="https://github.com/user-attachments/assets/1d5d433c-bc7a-40ed-871f-29293df48d15" />

r2 Value:
<img width="356" height="30" alt="image" src="https://github.com/user-attachments/assets/7d43e2bc-ec36-4e6d-9b7a-10eb3e74f161" />

Data prediction :
<img width="379" height="49" alt="image" src="https://github.com/user-attachments/assets/00a4abcf-bf0c-48e3-a051-3cb7da5df1e3" />





## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
