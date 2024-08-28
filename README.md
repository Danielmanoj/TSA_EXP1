# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 24/08/2024

# AIM:
To Develop a python program to Plot a time series data (Atmospheric_Composition_O2/Soil_Microbial_Activity).
# ALGORITHM:
1. Import libraries: Import pandas, numpy, and matplotlib for data processing and plotting.
2. Load and prepare data: Read the dataset, convert the 'Date' column to datetime format, and sort the data by date.
3. Set index: Set the 'Date' column as the index of the DataFrame.
4. Plot the data: Plot 'Atmospheric_Composition_O2' over time using matplotlib.
5. Display the plot: Show the graph with appropriate labels and title.
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
A graph is generated showing the variation of 'Atmospheric_Composition_O2' over time.
The plot provides a visual representation of how atmospheric oxygen composition changes over the recorded dates.
