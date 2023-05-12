# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import dataset and get data info
2.check for null values
3.Map values for position column
4.Split the dataset into train and test set
5.Import decision tree regressor and fit it for data
6.Calculate MSE,R2 and y predict

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: 212220040040
RegisterNumber: A.Harini Shamlin
##program##
import pandas as pd
data=pd.read_csv("/content/Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
y=data[["Salary"]]
from sklearn.model_selection import  train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
*/

```

## Output:
![image](https://github.com/ATHDY005/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/84709944/12ea05a0-cb91-4280-8ae7-a397c9f44c19)
![image](https://github.com/ATHDY005/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/84709944/3052261e-a050-485f-b249-29f5e27ca73e)
![image](https://github.com/ATHDY005/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/84709944/13b6e460-c0ef-4535-956e-c4f621f0c824)
![image](https://github.com/ATHDY005/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/84709944/9192a07c-08aa-4922-92ac-cb8b7847f493)
![image](https://github.com/ATHDY005/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/84709944/f0120563-ddf3-49af-9345-7b5e79c93ebf)
![image](https://github.com/ATHDY005/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/84709944/0c87715f-6f69-4556-8e42-2baa21660c71)
![image](https://github.com/ATHDY005/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/84709944/535a5426-80a4-4271-ae04-cbcf81dcdbdc)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
