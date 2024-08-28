# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 24/08/2024

# AIM:
To Develop a python program to Plot a time series data (Atmospheric_Composition_O2/Soil_Microbial_Activity).
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
 
 
# Set a random seed for reproducibility
np.random.seed(0)
 
# Load your temperature dataset with columns
data = pd.read_csv('/content/astrobiological_activity_monitoring.csv')
 
# Make sure your  column is in datetime format
data['Date'] = pd.to_datetime(data['Date'])
 
# Sorting the data by date (if not sorted)
data = data.sort_values(by='Date')
 
# Resetting the index
data.set_index('Date', inplace=True)

# Visualize the data
plt.figure(figsize=(12, 6))
plt.plot( data['Atmospheric_Composition_O2'], label='Data')
plt.xlabel('Soil_Microbial_Activity')
plt.ylabel('Atmospheric_Composition_O2')
plt.legend()
plt.title('Atmospheric_Composition_O2')
plt.show()
```









# OUTPUT:
![WhatsApp Image 2024-08-28 at 09 13 28_938ba02b](https://github.com/user-attachments/assets/fdcf5c96-5469-4dc4-b859-e70f4f9d6ebf)






# RESULT:
Thus we have created the python code for plotting the time series of given data.
