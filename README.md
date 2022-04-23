# Implementation-of-Multivariate-Linear-Regression-Model-for-Sales-Prediction

## AIM:
To write a program to implement the multivariate linear regression model for sales prediction.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
import pandas as pd
import matplotlib.pyplot as plt
df=pd.read_csv('Advertising.csv')
df.head()
df.describe()
df.isnull().sum()
df.shape
x=df[["TV","Radio","Newspaper"]]
x
y=df["Sales"]
y
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2,random_state=101) 
from sklearn.linear_model import LinearRegression
l=LinearRegression()
l.fit(x_train,y_train)
y_pred=l.predict(x_test)
x_test
print("Regressor Slope: ",l.coef_[0])
print("Regressor intercept: ",l.intercept_)
y_pred
from sklearn import metrics
MSE=metrics.mean_squared_error(y_test,y_pred)
print("MSE is {}".format(MSE))
r2=metrics.r2_score(y_test,y_pred)
print("R squared error is {}".format(r2))
l.predict([[150.3,240.5,234.5]])
```

## Output:
![image](https://user-images.githubusercontent.com/70479123/161591638-56da3ea3-174b-48bc-a147-d10ad1ae65ff.png)

## Result:
Thus the program to implement the multivariate linear regression model for sales prediction is written and verified using python programming.
