# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Start the program
2. import pandas as pd and read required csv file
3. print data.head(),info(),isnull().sum()
4. import LabelEncoder and fit.transform data.position
5. import train_test_split and split the test and train datasets with test size=0.2 and random_state=2
6. import DecisionTreeReggressorand predict y_pred
7. import metrics and find mse and also find r2
8. then finally find dt.predict([[5,6]])
9. Stop the program.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: S Saichandran 
RegisterNumber:  212220040138
*/
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
y=data["Salary"]
from sklearn.model_selection import train_test_split
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
```

## Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](/data.head().PNG)

![Decision Tree Regressor Model for Predicting the Salary of the Employee](/Data.info().PNG)

![Decision Tree Regressor Model for Predicting the Salary of the Employee](/3data.isnull().PNG)

![Decision Tree Regressor Model for Predicting the Salary of the Employee](/4.LE.PNG)

![Decision Tree Regressor Model for Predicting the Salary of the Employee](/5.mse.PNG)

![Decision Tree Regressor Model for Predicting the Salary of the Employee](/6.r2.PNG)

![Decision Tree Regressor Model for Predicting the Salary of the Employee](/7.predict.PNG)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
