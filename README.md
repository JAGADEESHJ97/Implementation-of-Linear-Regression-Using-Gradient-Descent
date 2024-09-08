# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
1. Import the standard Libraries.
2.Set variables for assigning dataset values.
3.Import linear regression from sklearn.
4.Assign the points for representing in the graph.
```
## Program:
```
/*
Program to implement the linear regression using gradient descent.
Developed by:JAGADEESH J
RegisterNumber:212223110015

from google.colab import drive
drive.mount('/content/gdrive')
import numpy as np
import pandas as pd
from sklearn.metrics import mean_absolute_error,mean_squared_error
import matplotlib.pyplot as plt  
*/
```
## Dataset:
```
a=pd.read_csv('/content/gdrive/MyDrive/student_scores.csv')
a
```
## Output:
![Screenshot 2024-09-08 184741](https://github.com/user-attachments/assets/b976a4f0-fc63-44b1-b52f-39d7340c0714)
## Head and Tail:
```
print(a.head())
print(a.tail())
```
# Output:
![Screenshot 2024-09-08 185113](https://github.com/user-attachments/assets/9dee292c-18b8-4e2b-96a3-5c447a3805a3)
## Information of Dataset:
```
a.info()
```
## Output:
![Screenshot 2024-09-08 192503](https://github.com/user-attachments/assets/7100b333-ce2c-459e-b1a9-00d4d7ef04b3)
## x and y value:
```
x=a.iloc[:,:-1].values
print(x)
y=a.iloc[:,-1].values
print(y)
```
## Output:
![Screenshot 2024-09-08 192618](https://github.com/user-attachments/assets/319e3c33-e606-47fd-a61f-4e3f811cc123)
## Program:
```
m=0
c=0
l=0.0001
epochs=5000
n=float(len(x))
error=[]
for i in range(epochs):
  y_pred=m*x + c
  dm=(-2/n) * sum(x*(y-y_pred))
  dc=(-2/n) * sum(y-y_pred)
  m=m - l *dm
  c=c - l *dc
  error.append(sum(y-y_pred)**2)
```
## Display the Output and Error:
```
print(m, c)
type(error)
print(len(error))
```
## Output:
![image](https://github.com/user-attachments/assets/99d1734a-81ab-4f16-a5bb-537aac0adbb1)
## Graph Plotting:
```
plt.plot(range(0,epochs),error)
```
## Output:
![image](https://github.com/user-attachments/assets/45e64eea-7292-4d9f-ae0c-6edabb791766)









## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
