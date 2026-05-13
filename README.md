# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Load the dataset from a CSV file and separate the features and target variable, encoding any categorical variables as needed.
2.Scale the features using a standard scaler to normalize the data.
3.initialize model parameters (theta) and add an intercept term to the feature set.
4.Train the linear regression model using gradient descent by iterating through a specified number of iterations to minimize the cost function.
5.Make predictions on new data by transforming it using the same scaling and encoding applied to the training data.
## Program:
```
/*
Program to implement the linear regression using gradient descent.
Developed by: SATHISH S
RegisterNumber:212225040390
*/
/*
Program to implement the linear regression using gradient descent.
Developed by: LINCE GIYO L
RegisterNumber: 212225100023
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

data=pd.read_csv("50_Startups.csv")
X=data['R&D Spend'].values
y=data['Profit'].values

X=(X-X.mean())/X.std()
m=0
b=0
learning_rate=0.01
epochs=1000
n=len(X)

for i in range(epochs):
    y_pred=m*X+b

    #Graddients
    dm=(-2/n)*np.sum(X*(y-y_pred))
    db=(-2/n)*np.sum(y-y_pred)

    #Update
    m=m-learning_rate*dm
    b=b-learning_rate*db

print("Slope(m):",m)
print("Intercept(b):",b)

#predictions for plotting
y_pred=m*X+b

plt.scatter(X,y)
plt.plot(X,y_pred)

plt.xlabel("R&D Spend (Normalized)")
plt.ylabel("Profit")
plt.title("Gradient Descent on 50_Startups Dataset")
plt.show()
*/
```

## Output:
<img width="1485" height="754" alt="590840056-c2805e31-c344-42cc-9a9f-19e1633c5c4f" src="https://github.com/user-attachments/assets/b0454559-25b4-44b5-a8b8-fdfec7e2df73" />



## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
