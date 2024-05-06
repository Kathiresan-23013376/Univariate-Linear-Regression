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
#Program to implement univariate Linear Regression to fit a straight line using least squares.
#Developed by: KATHIRESAN K
#register number: 212223110021
```
```
import numpy as np
import matplotlib.pyplot as py
X=np.array(eval(input()))
Y=np.array(eval(input()))
Xmean=np.mean(X)
Ymean=np.mean(Y)
num,den=0,0
for i in range(len(X)):
    num+=((X[i]-Xmean)*(Y[i]-Ymean))
    den+=(X[i]-Xmean)**2
slope=num/den
b=Ymean-slope*Xmean
ypred=slope*X+b
print("Slope ",slope,"and","Value is ",ypred)
py.scatter(X,Y,color='red')
py.plot(X,ypred,color='blue')
py.show()
```
## Output
![Screenshot 2024-05-05 142945](https://github.com/Kathiresan-23013376/Univariate-Linear-Regression/assets/150008375/290180a8-5c98-4e31-8571-48b87c3cdf53)
![Screenshot 2024-05-05 143001](https://github.com/Kathiresan-23013376/Univariate-Linear-Regression/assets/150008375/22bf556d-ed78-4139-863a-e8331b698c70)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
