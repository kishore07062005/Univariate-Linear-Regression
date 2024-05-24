# EX-9: Implementation of Univariate Linear Regression
### DATE:

## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
#Developed By:Rahul M R
#Register Number:2305003005

import numpy as np
import matplotlib.pyplot as plt
X=np.array(eval(input()))
Y=np.array(eval(input()))
plt.scatter(X,Y,color="blue")
Xmean=np.mean(X)
Ymean=np.mean(Y)
num,den=0,0
for i in range(len(X)):
    num+=(X[i]-Xmean)*(Y[i]-Ymean)
    den+=(X[i]-Xmean)**2
m=num/den
c=Ymean=m*Xmean
print(m,c)
Y_pred=m*X+c
print(Y_pred)
plt.plot(X,Y_pred,color='red')
plt.show()
```
## Output
![image](https://github.com/RahulM2005R/Univariate-Linear-Regression/assets/166299886/08534f28-d05c-4fbb-b39a-d2d8814a721e)

![image](https://github.com/RahulM2005R/Univariate-Linear-Regression/assets/166299886/7e997f55-24b0-410f-8a8d-751ff3720146)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
