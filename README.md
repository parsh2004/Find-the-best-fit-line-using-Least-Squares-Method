# Implementation of Univariate Linear Regression
# AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

# EQUIPMENTS REQUIRED:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

# ALGORITHM:
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

# PROGRAM:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Parshwanath
RegisterNumber: 212221230073
*/



import matplotlib.pyplot as plt
x=[5,6,3,2,6,7,1,2]
y=[2,3,6,5,8,3,5,8]
plt.scatter(x,y)
plt.show()

## Least Square Method

import numpy as np
import matplotlib.pyplot as plt
X=np.array([0,1,2,3,4,5,6,7,8,9])
Y=np.array([1,3,2,5,7,8,8,9,10,12])
 #mean 
X_mean=np.mean(X)
print(X_mean)
Y_mean=np.mean(y)
print(Y_mean)
num=0
denum=0
for i in range(len(x)):
  num+=(X[i]-X_mean)*(Y[i]-Y_mean)
  denum+=(x[i]-X_mean)**2
m=num/denum
b=Y_mean-m*X_mean
print(m,b)
Y_pred=m*X+b
print("y pred:",Y_pred)
plt.scatter(X,Y)
plt.plot(X,Y_pred,color='pink')
plt.show()
```

# OUTPUT:


![pa1](https://user-images.githubusercontent.com/94222288/198822485-1333b271-3772-463e-b3f0-503005ead8e5.jpeg)
![pa2](https://user-images.githubusercontent.com/94222288/198822491-226d35aa-7890-4236-9f95-4c19a87ad34d.jpeg)


# RESULT:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
