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

*/
import numpy as np
import matplotlib.pyplot as plt

x = np.array([1,2,3,4,5], dtype=float)
y = np.array([2,4,5,4,5], dtype=float)

x_mean = np.mean(x)
y_mean = np.mean(y)

numerator = np.sum((x - x_mean) * (y - y_mean))
denominator = np.sum((x - x_mean) ** 2)

slope = numerator / denominator
print("SLOPE :", slope)

b = y_mean - slope * x_mean
print("INTERCEPT :", b)

y_pred = slope * x + b
print("VALUE :", y_pred)

new_x = float(input("Enter X value: "))
yy = slope * new_x + b
print("Predicted Y:", yy)

plt.scatter(x, y, label="Data Points")
plt.plot(x, y_pred, label="Best Fit Line")
plt.xlabel("X")
plt.ylabel("Y")
plt.legend()
plt.title("SIMPLE LINEAR REGRESSION")
plt.show()
```

## Output:
![best fit line](sam.png)
<img width="632" height="192" alt="image" src="https://github.com/user-attachments/assets/2254dc36-3d29-4be6-846b-0a4cdf40dd69" />
<img width="780" height="587" alt="image" src="https://github.com/user-attachments/assets/d409efb8-e6d8-4d90-9791-ff52bd036244" />


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.



