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

#Preprocessing Input data

x=np.array([0,1,2,3,4,5,6,7,8,9])
y=np.array([1,3,2,5,7,8,8,9,10,12])

plt.scatter(x,y)
plt.show()
```
```
#Building the model
x_mean=np.mean(x)
y_mean=np.mean(y)

num=0
den=0
for i in range(len(x)):
    num+=(x[i]-x_mean)*(y[i]-y_mean)
    den+=(x[i]-x_mean)**2
m=num/den
c=y_mean-m*x_mean
print(m,c)
```
```
#Making predicitions
y_pred=m*x+c
print(y_pred)

plt.scatter(x,y) #actual
#plt.scatter(x,y_pred,color='red')
plt.plot([min(x),max(x)],[min(y_pred),max(y_pred)],color='red') #predicted
plt.show()
```

## Output
<img width="1411" height="753" alt="image" src="https://github.com/user-attachments/assets/5074be1f-60ba-449f-9ed1-78c67fb017ba" />
<img width="1393" height="306" alt="image" src="https://github.com/user-attachments/assets/dbd438ff-63a1-4c92-976b-42fd91ef4b33" />
<img width="1339" height="767" alt="image" src="https://github.com/user-attachments/assets/fd64999d-4556-404a-94ab-0676864bb979" />

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
