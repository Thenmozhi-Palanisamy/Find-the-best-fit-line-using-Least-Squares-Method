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
 
![image](https://user-images.githubusercontent.com/114234865/202094319-f768b891-0003-4e00-acf0-22d63d29e81d.png)

4. Compute the y -intercept of the line by using the formula:
 
![image](https://user-images.githubusercontent.com/114234865/202094500-b010befc-096e-409f-bdff-84bddcd244ed.png)

5. Use the slope m and the y -intercept to form the equation of the line. 6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by  : BALAJI J
RegisterNumber: 212221230116

import numpy as np
import matplotlib.pyplot as plt
X=np.array(eval(input()))
Y=np.array(eval(input()))
Xmean=np.mean(X)
Ymean=np.mean(Y)
num,den=0,0
for i in range (len(X)):
    num+=(X[i]-Xmean)*(Y[i]-Ymean)
    den+=(X[i]-Xmean)**2
m=num/den
c=Ymean-m*Xmean
print(m,c)
Y_pred=m*X+c
print(Y_pred)
plt.scatter(X,Y)
plt.plot(X,Y_pred,color="red")
plt.show()

```
## Output:

![image](https://github.com/Balaji-Jothiramalingam/Find-the-best-fit-line-using-Least-Squares-Method/assets/114234865/e11b9494-46d6-4445-a32b-aa7bd091691e)

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
