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
'''
to fit a straight line using least squares
Developer name:Sana Fathima H
Register number:212223240145
'''
import numpy as np
import matplotlib.pyplot as plt
x=np.array([1,8,6,5,4,15,20,56,47,29])
y=np.array([47,9,25,36,12,78,69,71,23,56])
plt.scatter(x,y)
plt.show()
xmean=np.mean(x)
ymean=np.mean(y)
num=0
den=0
for i in range(len(x)):
num+=(x[i]-xmean)*(y[i]-ymean)
den+=(x[i]-xmean)**2
m=num/den
b=ymean-m*xmean
print(m,b)
ypred=m*x+b
print(ypred)
plt.scatter(x,y,color='blue')
plt.plot(x,ypred,color='black')
plt.show()





```
## Output
![alt text](<Screenshot 2024-05-08 090844.png>)

![alt text](image.png)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
