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

![Screenshot 2023-10-12 224222](https://github.com/Abrinnisha6/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118889454/fa3ada63-c51a-4970-a015-4bae843d989f)

### data.info() :

![Screenshot 2023-10-12 224317](https://github.com/Abrinnisha6/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118889454/81ab6bf9-1a05-47c3-a0b3-326a9128db00)

### isnull() & sum() function :

![Screenshot 2023-10-12 224409](https://github.com/Abrinnisha6/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118889454/75c5fc33-ffb1-40e9-b35c-6cf2aac31807)

### data.head() for Position :

![Screenshot 2023-10-12 224549](https://github.com/Abrinnisha6/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118889454/0f30faa4-5d10-4d92-af48-2c883186200b)

### MSE value :

![Screenshot 2023-10-12 224632](https://github.com/Abrinnisha6/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118889454/cd7d5944-856d-426c-97ac-85c14579ea78)

### R2 value :

![Screenshot 2023-10-12 224731](https://github.com/Abrinnisha6/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118889454/786ca748-9e78-450a-a159-9bd17c972077)

### Prediction value :

![Screenshot 2023-10-12 224817](https://github.com/Abrinnisha6/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118889454/ff936744-92dd-42d0-9d98-1b591fc7b5c2)


## Result :

Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
