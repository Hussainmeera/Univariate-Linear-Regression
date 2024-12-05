# Implementation of Univariate Linear Regression
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
import numpy as np
import matplotlib.pyplot as plt

x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])

plt.scatter(x,y)
plt.show()

xmean = np.mean(x)
ymean = np.mean(y)

num = 0
den = 0

for i in range(len(x)):
    num += (x[i]-xmean)*(y[i]-ymean)
    den += (x[i]-xmean)**2

m = num/den
b = ymean-m*xmean
print(m,b)

ypred = m*x + b
print(ypred)

plt.scatter(x,y,color='red')
plt.plot(x,ypred, color='blue')
plt.show()







```
## Output
![Screenshot 2024-12-05 181152](https://github.com/user-attachments/assets/48441921-1144-4a76-8ef9-16f54ed868bf)
![Screenshot 2024-12-05 181201](https://github.com/user-attachments/assets/e75a05f8-9ae4-48e8-89e7-09cafe1daed4)




## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
