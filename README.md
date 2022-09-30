# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: A.sharmila
RegisterNumber:  212221230094
*/
```
import numpy as np

import matplotlib.pyplot as plt

#assign input

x=np.array([8,2,11,6,5,4,12,9,6,1])

y=np.array([3,10,3,6,8,12,1,4,9,14])

#mean values of input

x_mean=np.mean(x)

print(x_mean)

y_mean=np.mean(y)

print(y_mean)

num=0

denum=0

for i in range(len(x)):

num+=(x[i]-x_mean)*(y[i]-y_mean)

denum+=(x[i]-x_mean)**2
#find m

m=num/denum

#find b

b=y_mean-m*x_mean

print(m,b)

#find y_pred

y_pred=m*x+b

print(y_pred)

#plot graph

plt.scatter(x,y)

plt.plot(x,y_pred,color='purple')

plt.show()

import numpy as np

import pandas as pd

dataset=pd.read_csv('Placement_Data.csv')

print(dataset.iloc[3])

print(dataset.iloc[0:4])

print(dataset.iloc[:,1:3])
~~~

## Output:
![Screenshot (208)](https://user-images.githubusercontent.com/94506182/193317451-07f74671-0ab9-4ee6-bbef-4425cb277200.png)





## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
