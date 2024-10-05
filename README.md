# Ex.No: 03   COMPUTE THE AUTO FUNCTION(ACF)
Date: 

### AIM:
To Compute the Auto Correlation Function (ACF) of the data i Daily Delhi climate test  for the first 35 lags to determine the model type to fit the data.

### ALGORITHM:
1. Import the necessary packages
2. Find the mean, variance and then implement normalization for the data.
3. Implement the correlation using necessary logic and obtain the results
4. Store the results in an array
5. Represent the result in graphical representation as given below.
### PROGRAM:
import pandas as pd

# Load the dataset
file_path = '/mnt/data/DailyDelhiClimateTest.csv'
data = pd.read_csv(file_path)

# Display the first few rows of the data to understand its structure
data.head()
import matplotlib.pyplot as plt
from statsmodels.graphics.tsaplots import plot_acf

# Extracting the meantemp column for ACF computation
meantemp = data['meantemp']

# Plotting ACF for the first 35 lags
plt.figure(figsize=(10,6))
plot_acf(meantemp, lags=35)
plt.title('Autocorrelation Function (ACF) for Mean Temperature')
plt.show()


### OUTPUT:

![Screenshot 2024-10-05 081752](https://github.com/user-attachments/assets/a6aeb285-98b2-441f-b77c-d6bcff4881eb)

### RESULT:
        Thus we have successfully implemented the auto correlation function in python.
