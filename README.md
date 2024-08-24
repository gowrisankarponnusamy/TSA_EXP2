### DEVELOPED BY : GOWRISANKAR P
### REG NO: 212222230041
### DATE :
# Ex.No: 02 LINEAR AND POLYNOMIAL TREND ESTIMATION
### AIM:
To Implement Linear and Polynomial Trend Estiamtion Using Python.

### ALGORITHM:
Import necessary libraries (NumPy, Matplotlib)

Load the dataset

Calculate the linear trend values using least square method

Calculate the polynomial trend values using least square method

End the program
### PROGRAM:
```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from numpy.polynomial.polynomial import Polynomial

data = pd.read_csv('MentalHealthSurvey.csv')

X = data['age'].astype(float)
Y = data['depression'].astype(float)

coeffs_linear = np.polyfit(X, Y, 1) 
linear_trend = np.polyval(coeffs_linear, X)

coeffs_poly = np.polyfit(X, Y, 2)
poly_trend = np.polyval(coeffs_poly, X)

plt.figure(figsize=(10, 6))

plt.scatter(X, Y, color='blue', label='Data Points')

plt.plot(X, linear_trend, color='red', label='Linear Trend')

plt.plot(X, poly_trend, color='green', label='Polynomial Trend (Degree 2)')

plt.title('Linear and Polynomial Trend Estimation')
plt.xlabel('Age')
plt.ylabel('Depression')
plt.legend()

plt.show()
```

### OUTPUT
![image](https://github.com/user-attachments/assets/adbe73c9-2fcd-4690-97e6-61f92cd6f28c)

### RESULT:
Thus the python program for linear and Polynomial Trend Estiamtion has been executed successfully.
