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
Developed by: Jayaseelan U
RegisterNumber:  212223220039
*/
```

# program:
```
import numpy as np
import matplotlib.pyplot as plt
x = np.array(eval(input()))
y = np.array(eval(input()))
plt.scatter(x,y)
plt.show()
print(x)
print(y)

xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0

for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2

m = num/den
b = ymean - m*xmean
print(m,b)

ypred = m*x+b
print(ypred)

plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()
```

## Output:
![Screenshot 2025-03-13 114523](https://github.com/user-attachments/assets/abe75fa2-d8f2-4abd-b301-a2cd07ba93b8)




## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
