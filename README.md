## Developed by : Pravin Raj A
## Register number : 212222240079
## Date: 

# Ex.No: 01A PLOT A TIME SERIES DATA

# AIM:
To Develop a python program to Plot a time series data for analysing Bitcoin price prediction.

# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Plot the data according to need and can be altered monthly, or yearly.
4. Display the graph.
# PROGRAM:
```python
import pandas as pd
import matplotlib.pyplot as plt

# Load the CSV file
file_path = '/content/BTC-USD(1).csv'  # Replace with your file path
df = pd.read_csv(file_path)

# Convert the Date column to datetime format
df['Date'] = pd.to_datetime(df['Date'])

# Sort the data by Date just in case
df = df.sort_values('Date')

# Plot the Close price over time
plt.figure(figsize=(12, 6))
plt.plot(df['Date'], df['Close'], label='Close Price', color='blue')
plt.title('Bitcoin Closing Price Over Time')
plt.xlabel('Date')
plt.ylabel('Close Price (USD)')
plt.grid(True)
plt.legend()
plt.show()

```

# OUTPUT:

![Screenshot 2024-08-24 214929](https://github.com/user-attachments/assets/bf44b9cf-10a3-4e09-b6c6-66e6bab4cf1f)


# RESULT:
Thus the python program for plotting a time series data was executed successfully.
