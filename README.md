# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: PRAVEENA N 
RegisterNumber: 212222040122  
*/
```
```
import pandas as pd
data=pd.read_csv("C:/Users/SEC/Downloads/Salary.csv")
data.head()
```
```
data.info()
```
```
data.isnull().sum()
```
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data['Position']=le.fit_transform(data['Position'])
data.head()
```
```
x=data[['Position','Level']]
y=data['Salary']
```
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
```
```
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier()
dt.fit(x_train,y_train)
y_predict=dt.predict(x_test)
```
```
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_predict)
mse
```
```
r2=metrics.r2_score(y_test,y_predict)
r2
```
```
dt.predict([[5,6]])
```
## Output:
![image](https://github.com/Praveenanagaraji22/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119393514/6e0d759d-64ed-40a1-905c-845345b7c61c)

![image](https://github.com/Praveenanagaraji22/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119393514/c9415381-21d8-4da2-8ca4-269cffa39cf7)

![image](https://github.com/Praveenanagaraji22/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119393514/764ad874-8dad-4775-8d19-a3474d5f2eb1)

![image](https://github.com/Praveenanagaraji22/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119393514/f7ee7fff-b7fc-44cb-8f1d-6afd14e73b9c)

![image](https://github.com/Praveenanagaraji22/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119393514/8cfe80a9-39e4-45e7-8c03-7744eb955fac)

![image](https://github.com/Praveenanagaraji22/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119393514/4492800a-1d04-40dc-a6e9-69bd06c63792)

![image](https://github.com/Praveenanagaraji22/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119393514/37583872-8b20-48fc-b3a7-3abf5caef90c)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
