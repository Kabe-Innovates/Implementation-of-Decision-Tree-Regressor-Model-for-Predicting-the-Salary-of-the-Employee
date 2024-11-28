# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas

2.Import Decision tree classifier

3.Fit the data in the model

4.Find the accuracy score


## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: 24900985  
RegisterNumber: KABELAN G K 
*/
```

```
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
```
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
```
```
x=data[["Position","Level"]]
x.head()
y=data["Salary"]
y.head()

```
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
```
```
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn.metrics import r2_score
r2=r2_score(y_test,y_pred)
```
```
print("R2 score:",r2)


```
```
dt.predict([[5,6]])
```


## Output:

![image](https://github.com/user-attachments/assets/a61bc2cc-84ea-456b-b431-6814e70f21e9)

![image](https://github.com/user-attachments/assets/b85ac197-8498-48ee-b61a-e1bfb45397ee)

![image](https://github.com/user-attachments/assets/eb0865da-4ded-400b-a133-5bd3868eb59c)

![image](https://github.com/user-attachments/assets/f2538dc7-b3d6-4927-9403-1ba953b50548)

![image](https://github.com/user-attachments/assets/6b53be8b-b5c2-4b09-a220-1ec50aea4747)





## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
