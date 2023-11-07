# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM :

To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required :

1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm :

### STEP 1 :

Import the standard libraries. 2.Upload the dataset and check for any null values using .isnull() function.

### STEP 2 :

Import LabelEncoder and encode the dataset.

### STEP 3 :

Import DecisionTreeRegressor from sklearn and apply the model on the dataset.

### STEP 4 :

Predict the values of arrays.

### STEP 5 :

Import metrics from sklearn and calculate the MSE and R2 of the model on the dataset 7.Predict the values of array.

### STEP 6 :

Apply to new unknown values.

## Program:

### Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

### DEVELOPED BY : Gumma Dileep Kumar

### REG NO :  212222240032

```
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()

data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position","Level"]]
x.head()

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

```
## Output :

### data.head() :
![ml_7 1](https://github.com/gummadileepkumar/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707761/e5a736bf-210f-48ec-ac1e-4c7be05b712a)



### data.info() :

![ml_7 2](https://github.com/gummadileepkumar/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707761/db43cdec-9663-4792-a584-616515e145dc)


### isnull() & sum() function :

![ml_7 3](https://github.com/gummadileepkumar/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707761/a4a70181-7420-423f-8798-648285d3b622)


### data.head() for Position :


![ml_7 4](https://github.com/gummadileepkumar/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707761/b1925739-1c45-452a-b45b-bd19914c3167)


### MSE value :

![ml_7 5](https://github.com/gummadileepkumar/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707761/c0c3de8a-05fa-4c21-993f-0bfcb6566d1f)


### R2 value :

![ml_7 6](https://github.com/gummadileepkumar/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707761/f4375074-1897-4a12-ac8e-693a0e74442d)



### Prediction value :


![ml_7 7](https://github.com/gummadileepkumar/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707761/16fbfe52-63e5-4417-a529-d66d9a2455f1)


## Result :

Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
