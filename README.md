# Ex.No: 02 LINEAR AND POLYNOMIAL TREND ESTIMATION
Date:
### AIM:
To Implement Linear and Polynomial Trend Estiamtion Using Python.

### ALGORITHM:
1.Import necessary libraries (NumPy, Matplotlib)

2.Load the dataset

3.Calculate the linear trend values using least square method

4.Calculate the polynomial trend values using least square method

5.End the program

### PROGRAM:
A - LINEAR TREND ESTIMATION
```python
X = [i - years[len(years) // 2] for i in years]
x2 = [i ** 2 for i in X]
xy = [i * j for i, j in zip(X, tamil_nadu_values)]
n = len(years)
b = (n * sum(xy) - sum(tamil_nadu_values) * sum(X)) / (n * sum(x2) - (sum(X) ** 2))
a = (sum(tamil_nadu_values) - b * sum(X)) / n
linear_trend = [a + b * X[i] for i in range(n)]
print("Slope (b):", b)
print("Intercept (a):", a)
print("Linear Trend Values:", linear_trend
```

B- POLYNOMIAL TREND ESTIMATION
```python
x3 = [i ** 3 for i in X]
x4 = [i ** 4 for i in X]
x2y = [i * j for i, j in zip(x2, tamil_nadu_values)]

coeff = [[len(X), sum(X), sum(x2)],
         [sum(X), sum(x2), sum(x3)],
         [sum(x2), sum(x3), sum(x4)]]

Y = [sum(tamil_nadu_values), sum(xy), sum(x2y)]
A = np.array(coeff)
B = np.array(Y)
print("Polynomial Trend Equation: y = {:.2f} + {:.2f}x + {:.2f}x^2".format(a_poly, b_poly, c_poly))
```

### OUTPUT
### Trend equtions

![image](https://github.com/user-attachments/assets/7f355006-6f57-43fd-baa4-1638a0f1c47d)

A - LINEAR TREND ESTIMATION

![image](https://github.com/user-attachments/assets/bc2f35c6-9056-4e92-a0fa-344f174d9883)


B- POLYNOMIAL TREND ESTIMATION

![image](https://github.com/user-attachments/assets/883dec2f-cd25-4458-9027-45c274f6ab5a)


### RESULT:
Thus the python program for linear and Polynomial Trend Estiamtion has been executed successfully.
